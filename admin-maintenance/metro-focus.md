---
description: The metro section in the admin section consists of the following models
---

# Metro Focus

* [Category](metro-focus.md#category)
* [Financial Year](metro-focus.md#financial-year)
* [Indicators](metro-focus.md#indicators)
* [Indicator Elements](metro-focus.md#indicator-elements)
* [Indicator Quarter Results](metro-focus.md#indicator-quarter-results)
* [Update Files](metro-focus.md#update-files)

## Category

This section contains the thematic areas of the metro focus feature

![Thematic areas for metro focus](../.gitbook/assets/categories.png)

### Adding a new category

1. Click on the Add Category+ button on the top right.
2. Add the name and code. The combination of the name and code has to be unique.
3. Click on save.

## Financial Year

Financial years are setup in this section. Only one financial year can be active at a given time, this is marked by the check mark in the active column. The quarter column shows the latest active quarter for that financial year.

![Financial Year Section](../.gitbook/assets/financial_years.png)

### Adding a new financial year.

1. Click on the Add Financial Year+ button on the top right.
2. Add the budget year, the format must be same as the previous financial years.
3. If you want to make this financial year active, you first have to mark the other financial years as inactive
4. You can leave out the quarter field, if the financial year will not be the active one.
5. Click on save.

## Indicators

This section contains all the indicators and their details relating to the metro focus. Each indicator must have a unique code assigned to it.

![Indicator Section](../.gitbook/assets/indicator.png)

### Adding a new Indicator

1. Click on the Add Indicator+ button on the top right.
2. Populate the fields.

   The following fields must be populated and are used to determine which indicators will be shown on the metro performance page.

   1. Category
   2. Code
   3. Name
   4. Tier
   5. Frequency
   6. Goal

3. Click on save.

## Indicator Elements

Indicators are made up of elements which produce the required calculations for indicators  These are currently not used in the application

## Indicator Quarter Results

This section shows the performance results for a metro, for a particular financial year. 

![](../.gitbook/assets/results.png)

See[ Update Files](metro-focus.md#update-files) section to add new performance results.

## Update Files

Performance data is released quarterly and can be uploaded in this section

![Update Files Section](../.gitbook/assets/update_file.png)

### Downloading Quarterly data \(From IBER\)

To get access to this site, contact the project manager.

1. Click on Admin
2. Click on File Imports
3. Select Municipality with the relevant quarter
4. Download File.

The downloaded file should look as follows 

{% file src="../.gitbook/assets/template.xlsx" caption="Performance Template for Metros" %}



### Cleaning Imported Data.

Before importing the file into Municipal Money, the downloaded file has to be cleaned up a bit to make it easier to process.

1. Remove rows 1-4 such the the column headings are in the first row.
2. Remove row 9 containing "C88 OUTPUT INDICATORS FOR QUARTERLY REPORTING".
3. Remove row 55 containing "BACK-TO-BASICS REPORTING INDICATORS FOR COGTA BY REQUEST".
4. Remove row 73 containing "C88 OUTCOME INDICATORS WITH QUARTERLY FOR QUARTERLY REPORTING"
5. Remove row 100 containing "SIGNED: CITY MANAGER"
6. Save the file as a csv.

### Adding new quartley file

1. Click on ADD UPDATE FILE+
2. Add the financial year.
3. Add the quarter in which the performance date relates to.
4. Add the municiplaity, currently only metropolitian areas are shown.
5. Add the cleaned csv file that was process in the previous section.
6. Click on save.

The file will be processed in the background, in could take a few minutes to complete. Once the file has been process, a status will be shown next to the file to show whether it was successfully processed or not.

