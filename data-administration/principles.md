# Data Principles

## Input data formats

All input mechanisms for data will be built to accept the simplest lossless format, which in this case will be a CSV file with the first line indicating column headings.

The following points combined provide the reasoning for this choice:

1. The simplest data format is easiest to transform into more complex formats required by other tools. An example of this would be importing a CSV file into Microsoft Excel in order to use the data in the associated format.
2. At some point a data supplier can decide to alter the format of the data, which would make an input method dedicated to that data format obsolete.
3. It requires less effort for an administrator to export data from a more complex data format to the simplest format.
4. Less effort is required for a data supplier to switch to providing data in a simpler format, and doing so would also make the data compatible with more workflows.
5. A simpler format provides less opportunity for the same data to be stored in varying forms.

Text fields must not have duplicate spaces as this can effect how data points are created or updated e.g. the text used to identify the role of a municipal staff member in the contact details file

CSV files must use the UTF-8 encoding (as opposed to Excel's default cp1250 or Windows-1252). You can [use Notepad to convert to UTF-8](https://www.webtoffee.com/how-to-save-csv-excel-file-as-utf-8-encoded/#save-csv-notepad) since some versions of Excel do not actually save as UTF-8 even when selected in options.

Columns should be ordered as per the examples since some of the import options are based on column order and not column heading.

Column headings should match examples as some of the import options are based on column heading and not order.
