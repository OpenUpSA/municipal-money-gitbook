# Audit opinions and report URLs

Updating audit opinions requires updating the display year configuration for LAST\_OPINION\_YEAR before the profile build. See [display year config](fiscal-data/display-year-config.md#last\_opinion\_year) for more details.

Audit opinions can be found near the top of the municipalities scorecard page. Each audit year shows the audit feedback and a link to the report posted by treasury.

![](<../.gitbook/assets/image (14).png>)

To update the audit opinions select the Audit Opinion Facts Updates page in the Admin Dashboard to upload a CSV file of audit opinions.

![](<../.gitbook/assets/image (19).png>)

As shown in the [Standard Operating Procedures](standard-operating-procedure.md), updating audit opinions requires you to compile municipal profiles, please see the guide at [Compiling Municipal Profiles](administrators-guide.md#compiling-municipal-profiles).

### Data examples and formats

#### Audit opinion file example

report\_url should always start with http:// or https:// in order for the link to work correctly in the municipalities contact details.

```
demarcation_code,year,opinion_code,opinion_label,url
NMA,2020,qualified,Qualified,http://mfma.treasury.gov.za/Documents/07.%20Audit%20Reports/2019-20/01.%20Metros/NMA%20Nelson%20Mandela%20Bay/NMA%20Nelson%20Mandela%20Bay%20Consolidated%20Audit%20report%202019-20.pdf
CPT,2020,unqualified_emphasis_of_matter,Unqualified - Emphasis of Matter items,
```

#### Reference of opinion label to code mapping

`'Unqualified - With findings': 'unqualified_emphasis_of_matter'` should rather be `'Unqualified - Emphasis of Matter items': 'unqualified_emphasis_of_matter'`

```
    'Adverse opinion': 'adverse',
    'Disclaimer of opinion': 'disclaimer',
    'Qualified': 'qualified',
    'Unqualified - Emphasis of Matter items': 'unqualified_emphasis_of_matter',
    'Unqualified - No findings': 'unqualified',
    'Outstanding': 'outstanding',
```
