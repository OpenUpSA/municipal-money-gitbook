# Administrator's Guide

## Overview

This guide provides instructions both for updating the various types of data that is made available by the Municipal Money platform, as well as updating the contents of the compiled information for Municipal Profiles listed on the site.

For the purposes of this guide the data that can be managed using the administrative interface is split up into three types:

* Individual records
* Dimensional data
* Fiscal data

{% hint style="info" %}
Updating any of these types of data will immediately affect the data that is available on the platform, however, these changes will not immediately reflect on the Municipal Profiles listed on the site until a re-compilation of the Municipal Profiles is manually triggered, as demonstrated in the 'Compiling Municipal Profiles' section of this guide.
{% endhint %}

## Logging in

All the other sections of this guide will assume that you've already logged in to the admin interface using valid credentials, and that the account attached to these credentials have been assigned the appropriate rights for managing and updating data. If you don't have the required credentials or rights, please contact the administrator.

In order to login navigate to the following URL using your browser of choice: [https://municipalmoney.gov.za/admin](https://municipalmoney.gov.za/admin)

You will then be presented with the following login form where you can enter your provided username and password.

![](.gitbook/assets/login.png)

After successfully loggin in you will be presented with the home page of the administration site which should look similar to the following.

![](.gitbook/assets/screenshot-2020-12-18-at-11.17.19.png)

## Managing individual records

Functionality is provided for managing individual records of the following data:

* Geographies
* Demarcation Changes
* Municipal Staff Contacts

In order to see a list of the available records for one of these types, we need to click on the appropriate name of the data type listed on the administration home page. Let's use 'Geographies' as an example.

![](.gitbook/assets/screenshot-2021-02-22-at-06.00.10.png)

Here we see the 'Geographies' item as it's listed on the home page. Once we click on it we will be presented with a list of the available records.

![](.gitbook/assets/screenshot-2020-12-21-at-10.06.54.png)

From the listing screen we have the option of either creating a new record, using the 'ADD GEOGRAPHY' button, or viewing editing an existing record by clicking on one of the listed items.

## Managing dimensional data

The administration interface provides functionality for managing the following dimensional data:

* Aged Creditor Items \(v2\)
* Aged Debtor Items \(v2\)
* Cash Flow Items \(v2\)
* Income & Expenditure Items \(v2\)
* Capital Types \(v2\)
* Financial Position Items \(v2\)
* Government Functions \(v2\)
* Grant Types \(v2\)
* Repairs & Maintenance Items \(v2\)

This type of data has all the functionality that is available to individual records \(create and edit\), but is mostly encouraged to be edited in bulk by making use of the import/export functionality.

In order to see a list of the available records and options for one of these types, we need to click on the appropriate name of the data type listed on the administration home page. Let's use 'Aged Creditor Items \(v2\)' as an example.

![](.gitbook/assets/screenshot-2020-12-18-at-13.14.21.png)

Here we can see the 'Aged Creditor Items \(v2\)' item as it's listed on the home page. Once we click on it we will be presented with a list of records that is currently stored on the database.

![](.gitbook/assets/screenshot-2020-12-18-at-13.19.16.png)

As with individual records, we can edit and create records of 'Aged Creditor Items \(v2\)' data type from this screen. Since this data will mostly be provided in a file that we would prefer to upload in bulk, we'll look into the import function by clicking the 'IMPORT' button.

![](.gitbook/assets/screenshot-2020-12-21-at-10.36.48.png)

On this page we can select the file containing the data we wish to replace ALL our records with, along with it's format. We are also presented with the fields that are expected for each of the records.

Here is an example of a CSV file with acceptable data for this data type:

```text
code,label,position_in_return_form,return_form_structure,composition
0100,Bulk Electricity,1,line_item,
0200,Bulk Water,2,line_item,
0300,PAYE deductions,3,line_item,
0400,VAT (output less input),4,line_item,
0500,Pensions / Retirement deductions,5,line_item,
0600,Loan repayments,6,line_item,
```

Once the the selections are made and the 'SUBMIT' button is clicked you will be presented on details of the import you are attempting, and will be asked if you would like to continue with the import.

![](.gitbook/assets/screenshot-2020-12-21-at-10.43.26.png)

## Updating fiscal data

The administrative interface also provides the option for updating the following fiscal data:

* Aged Creditor Facts \(v2\)
* Aged Debtor Facts \(v2\)
* Audit Opinion Facts
* Capital Facts \(v2\)
* Cash Flow Facts \(v2\)
* Financial Position Facts \(v2\)
* Grant Facts \(v2\)
* Income & Expenditure Facts \(v2\)
* Repairs & Maintenance Facts \(v2\)
* UIFW Expense Facts

Unlike the data types mentioned before, these data types don't provide functionality for editing or creating individual records, and can only be updated in bulk by providing the appropriate CSV format.

We can see a list of the updates that have been provided by selecting the appropriate item from the listing on the administration home page. The name of the item would begin with the name of the data type and then be appended with the word 'Updates'. Let's use 'Aged Creditor Facts \(v2\) Updates' as an example.

![](.gitbook/assets/screenshot-2020-12-21-at-11.05.58.png)

Here we can see the 'Aged Creditor Facts \(v2\) Updates' item as it's listed on the home page. Once we click on it we will be presented with a list of of updates that have been applied to the 'Aged Creditor Facts \(v2\)' data in the past.

![](.gitbook/assets/screenshot-2020-12-21-at-11.08.39.png)

If we want to update the 'Aged Creditor Facts \(v2\)' data, we can do so by adding a new 'Update' record by clicking the 'ADD AGED CREDITOR FACTS \(V2\) UPDATE' button on the top right. You will then be presented with a screen where the file containing the update data can be specified.

![](.gitbook/assets/screenshot-2020-12-21-at-14.17.29.png)

The following is an example of a valid update file for the 'Aged Creditor Facts \(v2\)' data:

```text
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
Note that saving this new update can take quite a bit of time if the update file size is large. Be sure to give the browser a chance to upload the file, keeping the browser open and not navigating away from the loading page. 
{% endhint %}

![](.gitbook/assets/screenshot-2020-12-21-at-14.23.39.png)

After the creation of the new update, you should initially see that there is a placeholder value displayed in the place where the amount of deleted and inserted records will be displayed. These values will be populated once the update has completed.

Creating a new update starts off a task on the backend that processes the update. Refer to the 'Checking task status' chapter of this guide to find out more about tasks.

## Compiling municipal profiles

In order for the data made available by the Municipal Money platform to be displayed on the Municipal Profiles displayed on the site, a 'Municipal Profile Compilation' has to be initiated.

To see a list of previous compilations that were initiated, we can click on the appropriate item in on the home page.

![](.gitbook/assets/screenshot-2021-02-22-at-05.58.44.png)

Once we've click on the 'Municipality Profile Compilations' item, we will presented with a page where we can see previous compilations and create new ones.

![](.gitbook/assets/screenshot-2020-12-22-at-07.56.26.png)

Here we have a list of previous compilations, ordered by date, and an indication to the users that initiated the compilation and the periods that were targeted as the focus of the compilation. From this page we can make use of the 'ADD MUNICIPALITY PROFILE COMPILATION' button to initiate a new compilation.

![](.gitbook/assets/screenshot-2020-12-22-at-08.00.50.png)

At this point we can indicate the years that we would like to target during the compilation, with defaults provided from the system configurations discussed in the 'System configurations' chapter. Once we're happy with the years that we'd like to target we can initiate the compilation by clicking the 'SAVE' button.

![](.gitbook/assets/screenshot-2020-12-22-at-08.07.23.png)

We should now be redirected back to the page listing all the previous compilations, and our newly created compilation should now be included on the list.

Creating a new 'Municipality Profile Compilation' will start a task on the backend that processes the compilation. Refer to the 'Checking task status' chapter of this guide to find out more about tasks.

## Checking background task status

There are various circumstances in which lengthy operations need to run in the background. There two cases that have been mentioned earlier in this guide:

* Updating fiscal data
* Compiling municipal profiles

After initiating either of these actions a task will be started in the background. To view tasks that are currently running in the background we can navigate to the 'Queued tasks' section of the administration interface.

![](.gitbook/assets/screenshot-2020-12-22-at-09.07.29.png)

Here we have the 'Queued tasks' item as its listed on the home page. Clicking on this link should present us with a list of tasks that are currently being processed.

![](.gitbook/assets/screenshot-2020-12-22-at-09.07.04.png)

We can get an idea of the task that is running by looking in the 'NAME' column of the task. In this case we have a 'Municipal Profile Compilation' running.

Tasks that have completed will be removed from this list and will be moved to the 'Successful tasks' section. Navigating to this section from the home page will list all the successful tasks that was completed in the past.

![](.gitbook/assets/screenshot-2020-12-22-at-09.15.40.png)

From this list we can see that the last task that was successfully completed was a 'Aged Creditor Facts \(v2\) update' task.

## System configurations

In the case that there are settings that affect the whole system, they will usually be editable in the 'Config' section of the administrative interface. The following settings are currently available:

* GRANTS\_LATEST\_QUARTER
* GRANTS\_LATEST\_YEAR
* LAST\_AUDIT\_QUARTER
* LAST\_AUDIT\_YEAR
* LAST\_OPINION\_YEAR
* LAST\_UIFW\_YEAR

![](.gitbook/assets/screenshot-2020-12-22-at-09.23.37.png)

Here we see the 'Config' item on the home page. Clicking on it will take us to the 'Config' section of the administrative site.

![](.gitbook/assets/screenshot-2020-12-22-at-09.23.21.png)

On this page we have all the available settings listed along with a description and their current value. Clicking the 'SAVE' button here will apply these settings.

{% hint style="info" %}
Note that the changes applied to settings might only become visible on the site once a 'Municipality Profile Compilation' has been completed.
{% endhint %}

