# Principles

## Input data formats

All input mechanisms for data will be built to accept the simplest lossless format, which in this case will be a CSV file with the first line indicating column headings.

The following points combined provide the reasoning for this choice:

1. The simplest data format is easiest to transform into more complex formats required by other tools. An example of this would be importing a CSV file into Microsoft Excel in order to use the data in the associated format.
2. At some point a data supplier can decide to alter the format of the data, which would make an input method dedicated to that data format obsolete.
3. It requires less effort for an administrator to export data from a more complex data format to the simplest format.
4. Less effort is required for a data supplier to switch to providing data in a simpler format, and doing so would also make the data compatible with more workflows.
5. A simpler format provides less opportunity for the same data to be stored in varying forms.

