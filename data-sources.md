# Data Sources

## Financial data types

Original budget \(ORGB\) - Amount originally budgeted by the municipality

Adjusted budget \(AJDB\) - Amount budgeted after recommended adjustments

Preliminary outcome \(PAUD\) - Provided to auditors, but not yet processed and confirmed

Audited actual \(AUDA\) - Processed and confirmed by auditors

In-year actual \(M01 - M12\) - Provided by municipality, not yet confirmed by auditors

## Census

## Fiscal Delivery

* Cash flow
* Income & Expenditure
* Capital assets
* Capital expenditure
* Balance sheet

### Legacy

#### Structure

standard structured fiscal source

#### Provenance

* Municipality downloads Excel templates
* Municipality fills in excel templates
* Municipality Finance Manager signs off on filled-in files
* Municipality uploads signed-off files to Local Government database portal
* ??? data gets imported to some SQL database inside Treasury
* Snapshot is made of SQL database
* CSV extracts are exported from SQL database snapshot
* CSV extracts are \[provided to OpenUp project tehcnical lead via dropbox
* OpenUp uploads data to website

### Current \(since adoption of mSCOA\)

#### Structure

#### Provenance

* ?? muni has some integration to transfer data to treasury?
* Treasury aggregates data at the A1 schedule level \(but with multiple dimensions\)
* aggregates are provided to OpenUp via DropBox
* OpenUp uploads to website

## Local Government Database

1. ??Municipality submits to Auditor General??
2. Municipality submits to Local government Databse
3. OpenUp Downloads from Local Government Database portal
4. OpenUp imports to website

## National Treasury MFMA Portal

1. ??Municipality submits to Auditor General??
2. ??Municipality submits to Local government Databse
3. OpenUp scrapes from mfma.treasury.gov.za
4. OpenUp imports to website

