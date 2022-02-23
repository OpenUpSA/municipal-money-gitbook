---
description: >-
  The capital projects section (called infrastructure) in the admin section
  consists of the following models
---

# Capital Projects

## Projects

This section shows a list of all the capital projects.

![](../.gitbook/assets/projects.png)

### Adding new projects

Projects should generally not be added manually and are automatically populated from budget data uploads. See [Annual Spend Files (MTREF)](capital-projects.md#annual-spend-files-mtref) or [Quarterly Spend Files](capital-projects.md#quarterly-spend-files) on how to create and update budget data and watch [this walkthrough for uploading expenditures](capital-projects.md#undefined).

## Budget Phases

This section contains the various phases a budget has.

![](../.gitbook/assets/budget\_phases.png)

### Adding a new Budget Phase

1. &#x20;Click on ADD BUDGET PHASE+ button.
2. Enter a budget phase, it has to be unique.
3. Click on save.

## Expenditures

This section contains the budget phase expenditures for the capital projects.

![](../.gitbook/assets/expenditure.png)

### Adding a new expenditure

Expenditures should not be added manually. See [Annual Spend Files (MTREF)](capital-projects.md#annual-spend-files-mtref) or [Quarterly Spend Files](capital-projects.md#quarterly-spend-files)

## Financial Years

Financial years are set up in this section.&#x20;

![](../.gitbook/assets/financial\_year.png)

### Adding a new financial year

1. Click on ADD FINANCIAL YEAR+
2. Add a new financial year, make sure the format matches the other financial years.
3. Click on save.

## Project Quarterly Spends

This section contains the performance results for the metros

![Performance Results for metros](../.gitbook/assets/performance.png)

This data is represented by a chart at the bottom of the project details page as below. If a project does not have corresponding quarterly data, this chart will not be shown.

![](../.gitbook/assets/quarterlychart.png)

### Adding a new Quarterly Result

See [Quarterly Spend Files](capital-projects.md#quarterly-spend-files) for how to update the data

## Annual Spend Files (MTREF)

This section contains the budget and expenditure data.

![](../.gitbook/assets/annualspend.png)

The annual spend files are used to set the information in the Budget and Expenditure section on the project details page as shown below

![](../.gitbook/assets/projectdetails.png)

From the MTREF data each project is created using three identifiers namely the function, project description and project number columns. If all three of these match an existing project the budget values are updated from the upload. If any one of these identifiers do not match an existing project then a new project is created.

### Adding an annual spend file

To upload or update an annual spend file, select "Add annual spend file" at the top right of the page. You will see a page like that below.&#x20;

1\. Select the financial year, if the correct year does not exist, you can simply add it by clicking the green plus button.

2\. Select an Excel spreadsheet to upload

3\. Click save. Your upload will be sent to a queue to be processed. [See more about upload status here](capital-projects.md#status-of-uploaded-spend-files)

4\. To set which financial period to display projects for, change the value for CAPITAL\_PROJECT\_SUMMARY\_YEAR as described in the [Site date configuration](site-date-configuration.md)

![](../.gitbook/assets/addannual.png)

Below is an example of an annual spend file

{% file src="../.gitbook/assets/GT.xlsx" %}

## Quarterly Spend Files

This section shows how to upload new quarterly data for capital projects

![Quarterly spend section](../.gitbook/assets/spend\_file.png)

### Adding a new Quarterly spend file

Every quarter, national treasury will provide a file that will contain quarterly expenditures and totals of the projects and in some cases add new projects to the list. The file will look as follows.

{% file src="../.gitbook/assets/TSH.xls" %}
Capital Projects for Tshwane
{% endfile %}

1. Click on ADD QUARTERLY SPEND FILE+
2. Select a financial year and add the file that is provided from treasury.
3. Click on save.

The file will be processed in the background and will begin to populate the following sections

* Project
* Expenditure
* Project Quarterly Spends.

## Status of uploaded spend files

You can view the uploaded file under the Django Q | Succesful tasks as seen below

![](<../.gitbook/assets/Successful Upload (1).JPG>)

Any failed uploads can be viewed under the Django Q | Failed task as seen below

![](<../.gitbook/assets/Failed Upload (1).JPG>)

## Walkthrough for uploading expenditures

{% embed url="https://www.youtube.com/watch?v=8ASRvrjZCA4" %}

