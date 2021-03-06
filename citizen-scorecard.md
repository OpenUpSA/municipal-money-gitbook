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

**Sources:** [Census](data-sources.md#census)

## Description

### Mayor

**Sources:** [Local Government Database](data-sources.md#local-government-database)

### Mayoral staff

**Source:** [Local Government Database](data-sources.md#local-government-database)

### Contact details

**Sources:** [Local Government Database](data-sources.md#local-government-database)

### Office location

**Sources:** [Local Government Database](data-sources.md#local-government-database)

## Evaluative Performance

### Audit outcomes

**Sources:** [Local Government Database](data-sources.md#local-government-database)

**Trigger:** Project Lead indicates that data is uploaded, checked, and ready to use.

### Audit Reports

**Sources:** [National Treasury MFMA Portal](data-sources.md#national-treasury-mfma-portal)

**Trigger:** Project Lead indicates that data is uploaded, checked, and ready to use.

### Cash balance

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**Reference:** [State of Local Government Finances](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx)

#### Description

Cash balance at the end of the financial year.

#### Calculation

```text
= Cash available at year end
= [Cash Flow] item code 4200, Audited Actual
```

### Cash coverage

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** [State of Local Government Finances for 16 Oct 2019 \(page 10 - Indicator 2\)](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx), [Circular 71 \(page 7 - Section C.1\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### Description

Months of operating expenses can be paid for with the cash available.

#### Calculation

If Cash available at year end is negative, we say Cash Coverage is zero months.

```text
= Cash available at year end / Operating Expenditure per month
= [Cash Flow] item code 4200, Audited Actual / ([Income & Expenditure] item code 4600, Annual Audited Actual / 12)
```

### Spending of operating budget

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** N/A

#### Description

Difference between budgeted operating expenditure and what was actually spent.

#### Calculation

```text
= ((Actual Operating Expenditure - Budget Operating Expenditure) / Budgeted Operating Expenditure) * 100
= (([Income & Expenditure] item code 4600, Audited Actual - [Income & Expenditure] item code 4600, Adjusted Budget) / [Income & Expenditure] item code 4600, Adjusted Budget) * 100
```

### Spending of capital budget

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** [Circular 71 \(page 20 - Section 3.2\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### Description

Difference between budgeted capital expenditure and what was actually spent.

**Calculation**

```text
= ((Actual Capital Expenditure - Budgeted Capital Expenditure) / Budgeted Capital Expenditure) * 100
= (([Capital] item code 4100, Total Assets, Audited Actual - [Capital] item code 4100, Total Assets, Adjusted Budget) / [Capital] item code 4100, Total Assets, Adjusted Budget) * 100
```

### Spending on repairs and maintenance

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**Reference:** [State of Local Government Finances for 16 Oct 2019 \(page 14 - Indicator 4\)](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx), [Circular 71 \(page 4 - Section 1.A.3\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### **Description**

Spending on Repairs and Maintenance as a percentage of Property, Plant and Equipment.

**Calculation**

```text
= (Repairs and maintenance expenditure / (Property, Plant and Equipment + Investment Property)) * 100
= ([Capital] item code 4100, Audited Actual / ([Balance Sheet] item code 1300, Audited Actual + [Balance Sheet] item code 1401, Audited Actual)) * 100
```

### Fruitless and wasteful expenditure

**Sources:** [Local Government Database](data-sources.md#local-government-database), [Fiscal Delivery](data-sources.md#fiscal-delivery)

**Trigger:** Project Lead indicates that data is uploaded, checked, and ready to use.

**Reference:** [Circular 71 \(page 16 - Section 2.D.2\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### **Description**

Unauthorised, Irregular, Fruitless and Wasteful Expenditure as a percentage of operating expenditure.

#### Calculation

```text
= (Unauthorised, Irregular, Fruitless and Wasteful Expenditure / Actual Operating Expenditure) * 100
= ([Unauthorised, Irregular, Fruitless and Wasteful Expenditure] item codes irregular, fruitless, unauthorised / [Income & Expenditure] item code 4600, Audited Actual) * 100
```

### Current ratio

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** [Circular 71 \(page 7 - Section C.2\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx), [State of Local Government Finances \(page 24 - Indicator 12\)](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx)

#### Description

The value of a municipality's short-term assets as a multiple of its short-term liabilities.

#### Calculation

```text
= Current Assets / Current Liabilities
= [Balance Sheet] item code 2150, Audited Actual / [Balance Sheet] item code 1600, Audited Actual
```

### Liquidity ratio

**Source:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** [Municipal Budget and Reporting Regulations](http://mfma.treasury.gov.za/RegulationsandGazettes/Municipal%20Budget%20and%20Reporting%20Regulations/Pages/default.aspx), [State of Local Government Finances \(page 19 - Indicator 8\)](http://mfma.treasury.gov.za/Media_Releases/The%20state%20of%20local%20government%20finances/Pages/default.aspx)

#### Description

The municipality's immediate ability to pay its current liabilities.

#### Calculation

```text
= (Cash + Call Investment Deposits) / Current Liabilities
= [Balance Sheet] item codes 1800, 2200, Audited Actual / [Balance Sheet] item code 1600, Audited Actual
```

### Current debtors collection rate

**Source:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

**References:** [Municipal Budget and Reporting Regulations](http://mfma.treasury.gov.za/RegulationsandGazettes/Municipal%20Budget%20and%20Reporting%20Regulations/Pages/default.aspx), [Circular 71 \(page 5 - SectionB.1\)](http://mfma.treasury.gov.za/Circulars/Pages/Circular71.aspx)

#### Description

The percentage of new revenue \(generated within the financial year\) that a municipality actually collects.

#### Calculation

```text
= (Collected Revenue / Billed Revenue) * 100
= ([Cash Flow] item codes 3010, 3020, 3030, 3040, 3050, 3060, 3070, 3100, Audited Actual / [Income and Expenditure] item code 0200, 0300, 0400, 1000 less item code 2000, Audited Actual) * 100
```

## Income

## Spending

### Staff wages and salaries

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

#### Description

Staff salaries and wages as a percentage of operating expenditure.

#### Calculation

```text
= Wages & Salaries + Social Contributions / Actual Operating Expenditure
= [Income & Expenditure] item codes 3000, 3100, Audited Actual / [Income & Expenditure] item code 4600, Audited Actual
```

### Contractor Services

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

#### Description

Costs of contractor services as a percentage of operating expenditure.

#### Calculation

```text
= Contracted Services / Actual Operating Expenditure
= [Income & Expenditure] item code 4200, Audited Actual / [Income & Expenditure] item code 4600, Audited Actual
```

### What is money spent on?

**Sources:** [Fiscal Delivery](data-sources.md#fiscal-delivery)

## Household bills

**Sources:** [Local Government Database](data-sources.md#local-government-database)

