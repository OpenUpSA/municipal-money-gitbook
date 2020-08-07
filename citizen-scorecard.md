---
description: >-
  This document outlines the various aspects and indicators related to
  municipalities that will be presented on the citizen scorecard, and how this
  information is obtained and calculated.
---

# Citizen Scorecard

## Overview

### Name

### Province

### Basic demographics

## Description

Provenance

1. Municipality submits to Local government Databse
2. OpenUp Downloads from Local Government Database portal
3. OpenUp imports to website

### Mayor

### Mayoral staff

### Contact details

### Office location

## Evaluative Performance

### Audit outcomes

Provenance

1. ??Municipality submits to Local government Databse
2. OpenUp Downloads from Local Government Database portal
3. OpenUp imports to website

### Audit Reports

Provenance

1. ??Municipality submits to Local government Databse
2. OpenUp scrapes from mfma.treasury.gov.za
3. OpenUp imports to website

### Cash balance

#### Description

Cash balance at the end of the financial year.

#### Reference

[State of Local Government Finances](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx)

#### Source

standard structured fiscal source

Legacy \(pre-mSCOA\)

* Municipality downloads Excel templates
* Municipality fills in excel templates

Municipality Finance Manager signs off on filled-in files

Municipality uploads signed-off files to Local Government database portal

??? data gets imported to some SQL database inside Treasury

Snapshot is made of SQL database

CSV extracts are exported from SQL database snapshot

CSV extracts are \[provided to OpenUp project tehcnical lead via dropbox

* OpenUp uploads data to website

**mSCOA process**

* ?? muni has some integration to transfer data to treasury?
* Treasury aggregates data at the A1 schedule level \(but with multiple dimensions\)
* aggregates are provided to OpenUp via DropBox
* OpenUp uploads to website



#### Calculation

= Cash available at year end

= `Cash Flow` item code `4200`, `Audited Actual`

### Cash coverage

#### Description

Months of operating expenses can be paid for with the cash available.

#### Reference

[State of Local Government Finances](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx)

#### Source

#### Calculation

= Cash available at year end / Operating Expenditure per month

= Cash Flow item code 4200, Audited Actual / \(Income & Expenditure item code 4600, Annual Audited Actual / 12\)

If Cash available at year end is negative, we say Cash Coverage is zero months.

### Spending of operating budget

#### Description

Difference between budgeted operating expenditure and what was actually spent.

#### Reference

[Over and under spending reports to parliament](http://mfma.treasury.gov.za/Media_Releases/Reports%20to%20Parliament/Pages/default.aspx)

#### Source

#### Calculation

= \(Actual Operating Expenditure - Budget Operating Expenditure\) / Budgeted Operating Expenditure

= \(Income & Expenditure item code 4600, Audited Actual - Income & Expenditure item code 4600, Adjusted Budget\) / Income & Expenditure item code 4600, Adjusted Budget

### Spending of capital budget

#### Description

Difference between budgeted capital expenditure and what was actually spent.

#### **Reference**

[Over and under spending reports to parliament](http://mfma.treasury.gov.za/Media_Releases/Reports%20to%20Parliament/Pages/default.aspx)

#### **Source**

**Calculation**

= \(Actual Capital Expenditure - Budgeted Capital Expenditure\) / Budgeted Capital Expenditure

= \(Capital item code 4100, Total Assets, Audited Actual - Capital item code 4100, Total Assets, Adjusted Budget\) / Capital item code 4100, Total Assets, Adjusted Budget

### Spending on repairs and maintenance

#### **Description**

Spending on Repairs and Maintenance as a percentage of Property, Plant and Equipment.

#### **Reference**

[Circular 71](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### **Source**

**Calculation**

= Repairs and maintenance expenditure / \(Property, Plant and Equipment + Investment Property\)

= Capital Acquisition item code 4100, Audited Actual / \(Balance Sheet item code 1300, Audited Actual + Balance Sheet item code 1401, Audited Actual\)

### Fruitless and wasteful expenditure

#### **Description**

Unauthorised, Irregular, Fruitless and Wasteful Expenditure as a percentage of operating expenditure.

#### **Reference**

[Circular 71](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### Source

Provenance

1. ??Municipality submits to Auditor General??
2. Project Lead indicates to OpenUp that data is uploaded, checked, and ready to use on Local Government Database portal.
3. OpenUp Downloads from Local Government Database portal
4. OpenUp imports to website

#### Calculation

= Unauthorised, Irregular, Fruitless and Wasteful Expenditure / Actual Operating Expenditure

= Unauthorised, Irregular, Fruitless and Wasteful Expenditure item codes irregular, fruitless, unauthorised / Income & Expenditure item code 4600, Audited Actual

### Current ratio

#### Description

The value of a municipality's short-term assets as a multiple of its short-term liabilities.

#### Reference

[Circular 71](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### Calculation

= Current Assets / Current Liabilities

= Balance Sheet item code 2150, Monthly Actual / Balance Sheet item code 1600, Monthly Actual

### Liquidity ratio

#### Description

The municipality's immediate ability to pay its current liabilities.

#### Reference

[Municipal Budget and Reporting Regulations](http://mfma.treasury.gov.za/RegulationsandGazettes/Municipal%20Budget%20and%20Reporting%20Regulations/Pages/default.aspx)

#### Calculation

= \(Cash + Call Investment Deposits\) / Current Liabilities

= Balance Sheet item codes 1800, 2200, Monthly Actual / Balance Sheet item code 1600, Monthly Actual

### Current debtors collection rate

#### Description

The percentage of new revenue \(generated within the financial year\) that a municipality actually collects.

#### Reference

[Municipal Budget and Reporting Regulations](http://mfma.treasury.gov.za/RegulationsandGazettes/Municipal%20Budget%20and%20Reporting%20Regulations/Pages/default.aspx)

#### Calculation

= Collected Revenue / Billed Revenue

= Cash Flow item codes 3010, 3020, 3030, 3040, 3050, 3060, 3070, 3100, Monthly Actual / Income and Expenditure item code 0200, 0300, 0400, 1000 less item code 2000, Monthly Actual

## Income

## Spending

### Staff wages and salaries

#### Description

Staff salaries and wages as a percentage of operating expenditure.

#### Calculation

= Wages & Salaries + Social Contributions / Actual Operating Expenditure

= Income & Expenditure item codes 3000, 3100, Audited Actual / Income & Expenditure item code 4600, Audited Actual

### Contractor Service

#### Description

Costs of contractor services as a percentage of operating expenditure.

#### Calculation

= Contracted Services / Actual Operating Expenditure

= Income & Expenditure item code 4200, Audited Actual / Income & Expenditure item code 4600, Audited Actual

## Household bills



Provenance

1. ???Municipality submits to Local government Databse
2. Data files emailed to OpenUp project technical lead
3. OpenUp imports to website

