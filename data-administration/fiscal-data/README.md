---
description: >-
  Fiscal data is presented in the financial performance section of a municipal
  scorecard. This includes the update process for for Unauthorised, Irregular,
  Fruitless and Wasteful expenditure.
---

# Fiscal Data

{% hint style="info" %}
_**v2 cube uploads must NOT contain data for financial years before 2019-20**_
{% endhint %}

Updating fiscal data requires updating the display year configuration for GRANTS\_LATEST\_QUARTER, GRANTS\_LATEST\_YEAR, LAST\_AUDIT\_YEAR and LAST\_UIFW\_YEAR. See [display year config](display-year-config.md#grants\_latest\_quarter) for more details.

### Local Government Database

The administrative interface provides the option for updating the following fiscal data:

* Aged Creditor Facts (v2)&#x20;
* Aged Debtor Facts (v2)
* Capital Facts (v2)
* Cash Flow Facts (v2)
* Financial Position Facts (v2)
* Grant Facts (v2)
* Income & Expenditure Facts (v2)
* Repairs & Maintenance Facts (v2)

These data types don't provide functionality for editing or creating individual records, and can only be updated in bulk by providing the appropriate CSV format.

We can see a list of the updates that have been provided by selecting the appropriate item from the listing on the administration home page. The name of the item would begin with the name of the data type and then be appended with the word 'Updates'. Let's use 'Aged Creditor Facts (v2) Updates' as an example.

![](<../../.gitbook/assets/Screenshot 2020-12-21 at 11.05.58.png>)

Here we can see the 'Aged Creditor Facts (v2) Updates' item as it's listed on the home page. Once we click on it we will be presented with a list of of updates that have been applied to the 'Aged Creditor Facts (v2)' data in the past.

![](<../../.gitbook/assets/Screenshot 2020-12-21 at 11.08.39.png>)

If we want to update the 'Aged Creditor Facts (v2)' data, we can do so by adding a new 'Update' record by clicking the 'ADD AGED CREDITOR FACTS (V2) UPDATE' button on the top right. You will then be presented with a screen where the file containing the update data can be specified.

![](<../../.gitbook/assets/Screenshot 2020-12-21 at 14.17.29.png>)

The following is an example of a valid update file for the 'Aged Creditor Facts (v2)' data:

```
demarcation_code,period_code,g1_amount,l1_amount,l120_amount,l150_amount,l180_amount,l30_amount,l60_amount,l90_amount,total_amount,financial_year,period_length,financial_period,amount_type,item
CPT,2018AUDA,-1058474965,0,0,0,0,0,0,0,-1058474965,2018,year,2018,3,1
CPT,2018AUDA,-29195947,0,0,0,0,0,0,0,-29195947,2018,year,2018,3,2
CPT,2018AUDA,-32253,0,0,0,0,0,0,0,-32253,2018,year,2018,3,3
JHB,2018AUDA,0,0,0,0,0,0,1352620000,0,1352620000,2018,year,2018,3,1
JHB,2018AUDA,0,0,0,0,0,0,0,0,0,2018,year,2018,3,2
JHB,2018AUDA,0,0,0,0,0,0,0,0,0,2018,year,2018,3,3
NMA,2018AUDA,182407,0,0,0,0,0,0,0,182407,2018,year,2018,3,1
NMA,2018AUDA,0,0,0,0,0,0,0,0,0,2018,year,2018,3,2
NMA,2018AUDA,31791016,0,0,0,0,0,0,0,31791016,2018,year,2018,3,3
```

Once the file is selected and the 'SAVE' button is clicked you will once again be presented with the list of recent updates, which should now include your latest update.

{% hint style="info" %}
Note that saving this new update can take quite a bit of time if the update file size is large. Be sure to give the browser a chance to upload the file, keeping the browser open and not navigating away from the loading page.&#x20;
{% endhint %}

![](<../../.gitbook/assets/Screenshot 2020-12-21 at 14.23.39.png>)

After the creation of the new update, you should initially see that there is a placeholder value displayed in the place where the amount of deleted and inserted records will be displayed. These values will be populated once the update has completed.

Creating a new update starts a task on the backend that processes the update. Refer to the '[Checking task status](../administrators-guide.md#checking-background-task-status)' section of this guide to find out more about tasks.

### Unauthorised, Irregular, Fruitless and Wasteful (UIFW)

This can be found as one of the indicators on the municipal scorecard

![](<../../.gitbook/assets/image (35).png>)

Select the UIFW Expense Facts Updates page in the Admin Dashboard to upload a CSV file of UIFW data.

![](<../../.gitbook/assets/image (30).png>)

#### UIFW data example

```
"DEMARCATION_CDE","YEARPERIOD","UIFW_CDE","UIFW_LABEL","TCOST"
"BUF","2019","fruitless","Fruitless and Wasteful Expenditure",12378750
"BUF","2019","irregular","Irregular Expenditure",132542939
"BUF","2019","unauthorised","Unauthorised Expenditure",42977417
```
