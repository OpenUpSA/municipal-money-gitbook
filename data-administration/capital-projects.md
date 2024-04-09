---
description: >-
  The capital projects section (called infrastructure) in the admin section
  consists of the following models
---

# Capital Projects

Updating capital projects requires updating the display year configuration for CAPITAL\_PROJECT\_SUMMARY\_YEAR before the profile build. See [display year config](fiscal-data/display-year-config.md#last\_opinion\_year) for more details.

## Walkthrough for uploading capital project data

{% embed url="https://www.youtube.com/watch?v=8ASRvrjZCA4" %}

## How to upload MTREF files (SA36)

This section contains the budget and expenditure data.

![](../.gitbook/assets/annualspend.png)

From the MTREF data, each project is created using three identifiers namely the function, project description and project number columns. If all three of these match an existing project the budget values are updated from the upload. If any one of these identifiers does not match an existing project then a new project is created.

To upload or update an annual spend file, select "Add annual spend file" at the top right of the page. You will see a page like that below.&#x20;

1\. Select the financial year, if the correct year does not exist, you can simply add it by clicking the green plus button.

2\. Select an Excel spreadsheet to upload

3\. Click save. Your upload will be sent to a queue to be processed. [See more about the upload status here](capital-projects.md#status-of-uploaded-spend-files)

4\. To set which financial period to display projects for, change the value for CAPITAL\_PROJECT\_SUMMARY\_YEAR as described in the [Site date configuration](site-date-configuration.md)

![](../.gitbook/assets/addannual.png)

Below is an example of an annual spend file

{% file src="../.gitbook/assets/GT.xlsx" %}

## How to upload Quarterly files (SC36)

This section shows how to upload new quarterly data for capital projects

![Quarterly spend section](../.gitbook/assets/spend\_file.png)

Every quarter, National Treasury will provide a quarterly expenditure file to update project spending data and in some cases add new projects to the list. The file will look as follows.

{% file src="../.gitbook/assets/TSH.xls" %}
Capital Projects for Tshwane
{% endfile %}

1. Click on ADD QUARTERLY SPEND FILE+
2. Select a financial year and add the file that is provided by treasury.
3. Click on save.

The file will be processed in the background and will begin to populate the following sections

* 'Projects'
* 'Expenditures'
* 'Project quarterly spends'

## Status of uploaded spend files

You can view the uploaded file under the Django Q | Succesful tasks as seen below

![](<../.gitbook/assets/Successful Upload.JPG>)

Any failed uploads can be viewed under the Django Q | Failed task as seen below

![](<../.gitbook/assets/Failed Upload.JPG>)

## Project details page

This shows how budget files control information on the project details page

![](../.gitbook/assets/final.png)

## How do I correct mistakes in the data

#### Re-uploading corrected file

The preferred method is to correct the data in the provided file and re-upload.

#### Manually on the administrator site

An admin can manually change values for each 'Project', 'Expenditure', and 'Project quarterly spend' however this is not recommended as subsequent uploads can override the changes.

## Financial Years

In case a financial period does not exist it can be added in the following way:

![](../.gitbook/assets/financial\_year.png)

### Adding a new financial year

1. Click on ADD FINANCIAL YEAR+
2. Add a new financial year and make sure the format matches the other financial years.
3. Click on save.
