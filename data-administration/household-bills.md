# Household Bills

* [Data set files](household-bills.md#data-set-files)
* [Budget Phases](household-bills.md#budget-phases)
* [Financial Years](household-bills.md#financial-years)
* [Household Bill Totals](household-bills.md#household-bill-totals)
* [Household Classes](household-bills.md#household-classes)
* [Household Service Totals](household-bills.md#household-service-totals)
* [Household Services](household-bills.md#household-services)

## Data Set Files

![Adding new household data](../.gitbook/assets/h\_dataset\_file.png)

### Adding new household data

{% hint style="info" %}
Uploading household data will clear historical data and only display the most recent upload
{% endhint %}

National Treasury will send datasets when there are updates to household totals. The expected structure is as follows

{% file src="../.gitbook/assets/national_bill_totals.csv" %}
National Bill Totals
{% endfile %}

{% file src="../.gitbook/assets/national_service_totals.csv" %}
National Service Totals
{% endfile %}

Using these files follow the steps below:

1. Click on ADD DATA SET FILE+
2. Add the split files.
3. The file type indicates what type of data is in the file.
4. Click on save.

The files with their data will be uploaded in the background.

## Budget Phases

This section contains the various budget phases

![Budget Phases](../.gitbook/assets/h\_budget.png)

### Adding a new budget phase

1. Click on ADD BUDGET PHASE+
2. Add a budget phase, it has to be a unique name.
3. Click on save.

## Financial Years

![Financial Years](../.gitbook/assets/h\_finance.png)

### Adding a new financial year

1. Click on ADD FINANCIAL YEAR+
2. Add a new year. Make sure the year matches the format of the previous financial years.
3. Click on save.

## Household Bill Totals

![](../.gitbook/assets/h\_bill\_total.png)

### Adding new bill totals

Bill totals should not be added manually, see [Data Set Files](household-bills.md#data-set-files)

## Household Service Totals

![](../.gitbook/assets/h\_service\_total.png)

### Adding new service totals

Service totals should not be added manually, see [Data Set Files](household-bills.md#data-set-files)

## Household Classes

![](../.gitbook/assets/h\_class.png)

### Adding a new household Class

1. Click on ADD HOUSEHOLD CLASS+
2. Add a new class.
   * The min and max value determine the threshold for each household class. If the data has values outside this range, it typically means that there are errors in the data. Values outside the bounds will not be shown. These bounds have been determined by National Treasury
3. Click on save.

## Household Services

![Household Services](../.gitbook/assets/h\_service.png)

### Adding a new household service

1. Click on ADD HOUSEHOLD SERVICE+
2. Add a service, the name must be unique.
3. Click on save.
