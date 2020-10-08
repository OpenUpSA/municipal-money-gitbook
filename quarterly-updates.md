# Quarterly updates

This covers how to keep the data up to date. Each quarter, as new data is released, the following needs to be done to update the data served by the API and the Citizen Scorecard. It's best to do this on a test database first and validate the results before updating the production database.

* Quarter 1
  * Contacts
  * Latest monthly actuals
  * Corrections all over
* Quarter 2
  * Contacts
  * Latest monthly actuals
  * Corrections all over
  * **Audited Annual data from last financial year**
* Quarter 3
  * Contacts
  * Latest monthly actuals
  * Corrections all over
  * **Audit outcomes for last financial year**
  * **Unauthorised, Irregular, and Fruitless and Wasteful expenditure from financial year before last**
* Quarter 4
  * Contacts
  * Latest monthly actuals
  * Corrections all over

### 

### Extract CSV datasets from Excel Spreadsheets

Install some additional dependencies:

* `source env/bin/activate`
* `pip install bs4` - bs4 is used to scrape audit report URLs
* `pip install csvkit` - optional - convenient tools for inspecting and querying CSVs

Extract CSV datasets from Excel Spreadsheets using the following scripts in `municipal_finance/data_import/`

* audit\_opinions.py
  * Go to the [local government database](https://lg.treasury.gov.za/iworld/default_prov.htm)
  * Budget Document Tracking - Reporting &gt; List Audit Opinion
  * Location Level: Municipality
  * Financial Year End\(s\): Control+Click the four years up to and including the last audit result available
  * Sort Options: By Municipality
  * Level of Detail: Summary
  * Demarcation: Current
  * Choose Excel 2000 report format
  * Process Request: The downloaded file has .xls extension but is html - open in libreoffice or excel and save explicitly as .xls again.
* contact\_details.py
  * Go to the [local government database](https://lg.treasury.gov.za/iworld/default_prov.htm)
  * Contacts - Reporting &gt; General Information - Municipalities Individuals
  * Choose 'Municipality' in the 'Location Level' field.
  * Choose the relevant roles in the 'Column Selection Form' field.
  * Choose 'BY Municipality' in the 'Sort Options' field.
  * Choose Excel 2000 report format
  * Download report, open in excel, save as xlsx \(the website gives HTML in .xls\)
  * Process Request: The downloaded file has .xls extension but is html - open in libreoffice or excel and save explicitly as .xls again.
* uifw\_expenditure.py
  * input files like [01. Irregular Expenditures - Master 04 December 2014](http://mfma.treasury.gov.za/Media_Releases/mbi/2014/Documents/G.%20Additional%20information)

### 

### Scrape the MFMA website for the Audit Report URLs into a CSV file

Using `municipal_finance/data_import/audit_reports.py`

### 

### Insert/update from CSV files

1. Update the paths in the per-cube files in `sql/upsert/`
2. Execute the files

* This takes about 30 minutes for incexp, a bit less for capital, and the rest are much quicker.

These files work as follows:

1. Create a temporary table
2. Import the CSV file to the temporary table
3. Delete all rows for which a matching demarcation code and period code occurs in the update dataset

* e.g. if BUF 2016AUDA is in the update, all BUF 2016AUDA rows will be deleted from the update dataset. That means line items that were removed from the Treasury Local Government Database and aren't in quarterly update datasets will also be removed from the Municipal Data database.
* if a demarcation code and period code is already in the database and not in the update dataset, it will remain in the Municipal Data database.

1. Insert all rows of the update dataset to the fact table

* `period_code` is decoded into `financial_period`, `financial_year`, `amount_type` on the fly. Unexpected values result in SQL errors, aborting the transaction.

Update the last-updated date in the model files for each cube in `models/*.json`

Update the materialised view data using `bin/materialised_views.py`:

You might need to allow extra open files with something like `ulimit -n 500000`

1. Run with --profiles-from-api to update the muni-specific profile data

* This takes about 6 minutes locally

1. Run with --calc-medians and --calc-rating-counts to update comparison data based on profile changes.
2. Check what changed using `git diff` and commit commit if changes look right.
3. Run `bin/test-pages.sh` and ensure that all pages return "200 OK"

### 

### Annual data

Whenever Audited Annual data becomes available \(AUDA financial data and Audit Outcomes\), adjust the years used by `scorecard/profile_data.py` to include the latest financial year available.

Audit outcomes will be captured in the months following 1 December following the end of the financial year. Audited figures can start being submitted by municipalities to Treasury from this point. That means new audited annual figures can appear from Q2.

Pre-audit figures are captured in the period 3 Aug to 30 Nov after the end of the financial year.

### 

### Quarterly data

Indicators using quarterly data automatically use the latest quarter available.

Quarterly Section 71 submissions are available 2 months after the end of the quarter.

### 

### Validating the data

The aim here is to ensure that the data is in the correct format, and that the import worked correctly, such that the correct values are shown to users of the site. That means the right number is returned, for a given line item, for a given period and municipality. The correct number is defined by what has been provided in the snapshot from Treasury. This can be sanity-checked by comparing to what's published on the MFMA website. Examples of the kind of errors this is trying to catch are:

* different number formats
* different line item codes
* different data structures which aren't detected by the database constraints, but can be detected by manually comparing the numbers presented to published documents

This shouldn't be exhaustive - when some numbers in each dataset match expected values, we can infer that the data is imported correctly. The strategy is to identify a few changes between subsequent snapshots, and check that they are reflected in the API. Since distinctions aren't made between importing different municipalities, other municipalities should be imported equivalently.

Check that the column order in the snapshots match those in the _"upsert"_ scripts. e.g.:

```text
head -1 2017q2/*
```

Quickly get an idea of what was updated in the datasets: compare this snapshot to the previous for each dataset:

e.g. with the command `diff <(sort ../../2016q4/Section\ 71\ Q4\ published\ data/bsheet_2016q4_acrmun.csv) <(sort bsheet_2017q1_acrmun.csv)|less` Search for `<` to find a row that was removed, paging past the period codes that fell out of the update window to some lines where one value was swapped for another. This example shows a value that was swapped from one item code to another, and a second change where a number changed by R1. Check that this change is correctly reflected in the API using the API itself or the table view where possible.

```text
3951c1901
< "DC12","2015AUDA","1400",128859696.00
---
> "DC12","2015AUDA","1400",1000.00
3958c1908
< "DC12","2015AUDA","1500",1000.00
---
> "DC12","2015AUDA","1500",128859696.00
3960c1910
< "DC12","2015AUDA","1650",4952698143.00
---
> "DC12","2015AUDA","1650",4952698144.00
```

Do each of these cursory tests for a small sample of municipalities to sanity-check. Focus on things you know have changed.

* Contact details
* Check that the website link works
* Check that contact details look ok
* Follow Audit report links on the Scorecard site and check that the link works, and that the opinion in the report matches what is shown on the page. For example, the heading "Basis for Qualified Opinion" seems to be around page 2 or 3 for a _Qualified_ opinion on the page. You can also find the [Audit Reports on the MFMA website](http://mfma.treasury.gov.za/Documents/07.%20Audit%20Reports)
* Compare Original Budget \(ORGB\) values to [Adopted Budgets on the MFMA website](http://mfma.treasury.gov.za/Documents/03.%20Budget%20Documentation)
* Grants - Not all of them appear in our conditional grant dataset - compare those that do e.g. _Local Government Financial Management Grant_ - e.g. with `select l.name, f.amount from conditional_grants_facts f, conditional_grants l where f.grant_code = l.code and demarcation_code = 'CPT' and amount_type_code = 'ORGB' and financial_year = 2015 and period_length = 'year' order by l.name;` - If some values are close, e.g. 217,498,000 vs 217,548,000, the data is probably loaded correctly
* Operating Revenue and expenditure
* Compare Audited \(AUDA\) values to the [audited financial statements on the MFMA website](http://mfma.treasury.gov.za/Documents/05.%20Annual%20Financial%20Statements)
  * Use the _consolidated_ financial statements where available for municipalities with multiple entities
  * You can compare some values in the Scorecard site and the rest in the Table View
  * Debtor \(under Consumer Receivables\) and Creditor age analysis can be found in the AFS
  * Make sure to check unauthorised, irregular, fruitless and wasteful expenditure
* Compare in-year values to [Section 71 in-year reports](http://mfma.treasury.gov.za/Media_Releases/s71/Pages/default.aspx)
  * Use the API or the database for datasets not available in the Table View:
    * e.g. `select l.label, l30_amount from aged_debtor_facts f, aged_debtor_items l where f.item_code = l.code and demarcation_code = 'CPT' and financial_year = 2016 and financial_period = 09 and amount_type_code = 'ACT';`
  * Compare the latest available month of a quarter to the quarter value in the report

## 

## Upsert Log

### 

### 2016q4

* Some of the files had amounts ending .00 so to check that simply rounding was ok, I ran `grep -v '\.00' *|egrep -v "(capital|cflow|grants|rm_)"` - the excluded files didn't have .00 endings.

### 

### 2017q4

* cflow monthly amounts doubled from previous snapshots where they occurred. It turned out this was due to an issue in the query used to generate the snapshot and a new cflow snapshot was supplied.

### 

### 2018q1

* capital and creditor age had unexpected codes for one KZN muni. Marina said we should filter them out.

### 

### 2018q3

* The audit opinion label `Unqualified - With findings` should get mapped to `Unqualified - Emphasis of Matter items` - confirmed with Elsabe.

### 

### 2019-07-09 loading Section 71 Q3 2018-19

e.g. `cat sql/upsert/aged_debtor.sql | docker-compose run --rm postgres psql postgresql://postgres@postgres/municipal_finance`

