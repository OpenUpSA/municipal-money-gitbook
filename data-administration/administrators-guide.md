# Administrator's Guide

{% hint style="info" %}
_**v2 cube uploads must NOT contain data for financial years before 2019-20**_
{% endhint %}

## Overview

This guide provides instructions both for updating the various types of data that is made available by the Municipal Money platform, as well as updating the contents of the compiled information for Municipal Profiles listed on the site.

See also the [data principles](principles.md).

For the purposes of this guide the data that can be managed using the administrative interface is split up into three types:

* Individual records
* Dimensional data
* Fiscal data

{% hint style="info" %}
Updating any of these types of data will immediately affect the data that is available in the API, however, these changes will not immediately reflect on the Municipal Profiles listed on the site until a re-compilation of the Municipal Profiles is manually triggered, as demonstrated in the [Compiling Municipal Profiles](administrators-guide.md#compiling-municipal-profiles) section of this guide.
{% endhint %}

## Managing individual records

Functionality is provided for managing individual records of the following data:

* Geographies
* Demarcation Changes
* Municipal Staff Contacts

In order to see a list of the available records for one of these types, we need to click on the appropriate name of the data type listed on the administration home page. Let's use 'Geographies' as an example.

![](<../.gitbook/assets/Screenshot 2021-02-22 at 06.00.10.png>)

Here we see the 'Geographies' item as it's listed on the home page. Once we click on it we will be presented with a list of the available records.

![](<../.gitbook/assets/image (10).png>)

From the listing screen we have the option of either creating a new record, using the 'ADD GEOGRAPHY' button, or viewing editing an existing record by clicking on one of the listed items.

## Bulk updates

Functionality is provided to add and update geography records in bulk. To do this select ‘Geographies’ in the Scorecard section. Then choose import near the top right of the screen.

You should now see a page similar to that shown below. Here you can upload a file containing a list of geographies with any variation of columns shown below, remember to select CSV format.

![](<../.gitbook/assets/image (11).png>)

After submitting the file a page will display pending changes to the data, whereby you may review and accept the changes.

## Checking background task status

There are various circumstances in which lengthy operations need to run in the background. There are two cases that have been mentioned earlier in this guide:

* Updating fiscal data
* Compiling municipal profiles

After initiating either of these actions a task will be started in the background. To view tasks that are currently running in the background we can navigate to the 'Queued tasks' section of the administration interface.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 09.07.29.png>)

Here we have the 'Queued tasks' item as its listed on the home page. Clicking on this link should present us with a list of tasks that are currently being processed.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 09.07.04.png>)

We can get an idea of the task that is running by looking in the 'NAME' column of the task. In this case we have a 'Municipal Profile Compilation' running.

Tasks that have completed will be removed from this list and will be moved to the 'Successful tasks' section. Navigating to this section from the home page will list all the successful tasks that were completed in the past.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 09.15.40.png>)

From this list we can see that the last task that was successfully completed was the 'Aged Creditor Facts (v2) update' task.

