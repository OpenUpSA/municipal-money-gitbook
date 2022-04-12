# Administrator's Guide

{% hint style="info" %}
_**v2 cube uploads must NOT contain data for financial years before 2019-20**_
{% endhint %}

## Overview

This guide provides instructions both for updating the various types of data that is made available by the Municipal Money platform, as well as updating the contents of the compiled information for Municipal Profiles listed on the site.

See also the [data principles](../principles.md).

For the purposes of this guide the data that can be managed using the administrative interface is split up into three types:

* Individual records
* Dimensional data
* Fiscal data

{% hint style="info" %}
Updating any of these types of data will immediately affect the data that is available in the API, however, these changes will not immediately reflect on the Municipal Profiles listed on the site until a re-compilation of the Municipal Profiles is manually triggered, as demonstrated in the [Compiling Municipal Profiles](./#compiling-municipal-profiles) section of this guide.
{% endhint %}

## Managing individual records

Functionality is provided for managing individual records of the following data:

* Geographies
* Demarcation Changes
* Municipal Staff Contacts

In order to see a list of the available records for one of these types, we need to click on the appropriate name of the data type listed on the administration home page. Let's use 'Geographies' as an example.

![](<../../.gitbook/assets/Screenshot 2021-02-22 at 06.00.10.png>)

Here we see the 'Geographies' item as it's listed on the home page. Once we click on it we will be presented with a list of the available records.

![](<../../.gitbook/assets/image (10).png>)

From the listing screen we have the option of either creating a new record, using the 'ADD GEOGRAPHY' button, or viewing editing an existing record by clicking on one of the listed items.

### Data examples and formats

#### Municipal Staff Contacts

```
demarcation_code,role,title,name,office_number,fax_number,email_address
CPT,Secretary of Municipal Manager,Ms,Zakeelah Behardien,021 400 1331,086 202 9098,zakeelah.behardien@capetown.gov.za
CPT,Secretary of Financial Manager,Ms,Tarryn Bell,021 400 5021,021 400 5660,tarryn.bell@capetown.gov.za
CPT,Secretary of Mayor/Executive Mayor,Ms,Rushdia Walker,021 400 9481,086 201 1851,rushdia.walker@capetown.gov.za
CPT,Secretary of Deputy Mayor/Executive Mayor,Ms,Karen Haskell,021 400 2963,021 400 3368,Karen.Haskell@capetown.gov.za
CPT,Secretary of Speaker,Ms,Ilze Rheeder,021 400 2285,021 400 5864,Ilze.Rheeder@capetown.gov.za

```

### Audit opinions

Opinion code to label mapping

```
    'Adverse opinion': 'adverse',
    'Disclaimer of opinion': 'disclaimer',
    'Qualified': 'qualified',
    'Unqualified - Emphasis of Matter items': 'unqualified_emphasis_of_matter',
    'Unqualified - With findings': 'unqualified_emphasis_of_matter',
    'Unqualified - No findings': 'unqualified',
    'Outstanding': 'outstanding',
```

Data example

```
demarcation_code,year,opinion_code,opinion_label
CPT,2019,unqualified_emphasis_of_matter,Unqualified - Emphasis of Matter items
CPT,2020,unqualified_emphasis_of_matter,Unqualified - Emphasis of Matter items
```

## Bulk updates

Functionality is provided to add and update geography records in bulk. To do this select ‘Geographies’ in the Scorecard section. Then choose import near the top right of the screen.

You should now see a page similar to that shown below. Here you can upload a file containing a list of geographies with any variation of columns shown below, remember to select CSV format.

![](<../../.gitbook/assets/image (11).png>)

After submitting the file a page will display pending changes to the data, whereby you may review and accept the changes.

### Data examples and formats

#### Geography data

The only required column is the id. All other columns to be updated are optional

```
id,geo_level,geo_code,name,long_name,phone_number
171,municipality,TSH,City of Tshwane,"City of Tshwane, Gauteng",012 358 7911
154,municipality,BUF,Buffalo City,"Buffalo City, Eastern Cape",043 705 2000
```



## Updating fiscal data

The administrative interface also provides the option for updating the following fiscal data:

* Aged Creditor Facts (v2)
* Aged Debtor Facts (v2)
* Audit Opinion Facts
* Capital Facts (v2)
* Cash Flow Facts (v2)
* Financial Position Facts (v2)
* Grant Facts (v2)
* Income & Expenditure Facts (v2)
* Repairs & Maintenance Facts (v2)
* UIFW Expense Facts

Unlike the data types mentioned before, these data types don't provide functionality for editing or creating individual records, and can only be updated in bulk by providing the appropriate CSV format.

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

Creating a new update starts off a task on the backend that processes the update. Refer to the 'Checking task status' chapter of this guide to find out more about tasks.Data examples and formats

{% content-ref url="fiscal-data-import-table-structure-examples.md" %}
[fiscal-data-import-table-structure-examples.md](fiscal-data-import-table-structure-examples.md)
{% endcontent-ref %}

## Compiling municipal profiles

In order for the data made available by the Municipal Money platform to be displayed on the Municipal Profiles displayed on the site, a 'Municipal Profile Compilation' has to be initiated.

To see a list of previous compilations that were initiated, we can click on the appropriate item in on the home page.

![](<../../.gitbook/assets/Screenshot 2021-02-22 at 05.58.44.png>)

Once we've click on the 'Municipality Profile Compilations' item, we will presented with a page where we can see previous compilations and create new ones.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 07.56.26.png>)

Here we have a list of previous compilations, ordered by date, and an indication to the users that initiated the compilation and the periods that were targeted as the focus of the compilation. From this page we can make use of the 'ADD MUNICIPALITY PROFILE COMPILATION' button to initiate a new compilation.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 08.00.50.png>)

At this point we can indicate the years that we would like to target during the compilation, with defaults provided from the system configurations discussed in the 'System configurations' chapter. Once we're happy with the years that we'd like to target we can initiate the compilation by clicking the 'SAVE' button.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 08.07.23.png>)

We should now be redirected back to the page listing all the previous compilations, and our newly created compilation should now be included on the list.

Creating a new 'Municipality Profile Compilation' will start a task on the backend that processes the compilation. Refer to the 'Checking task status' chapter of this guide to find out more about tasks.

## Checking background task status

There are various circumstances in which lengthy operations need to run in the background. There two cases that have been mentioned earlier in this guide:

* Updating fiscal data
* Compiling municipal profiles

After initiating either of these actions a task will be started in the background. To view tasks that are currently running in the background we can navigate to the 'Queued tasks' section of the administration interface.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 09.07.29.png>)

Here we have the 'Queued tasks' item as its listed on the home page. Clicking on this link should present us with a list of tasks that are currently being processed.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 09.07.04.png>)

We can get an idea of the task that is running by looking in the 'NAME' column of the task. In this case we have a 'Municipal Profile Compilation' running.

Tasks that have completed will be removed from this list and will be moved to the 'Successful tasks' section. Navigating to this section from the home page will list all the successful tasks that was completed in the past.

![](<../../.gitbook/assets/Screenshot 2020-12-22 at 09.15.40.png>)

From this list we can see that the last task that was successfully completed was a 'Aged Creditor Facts (v2) update' task.

