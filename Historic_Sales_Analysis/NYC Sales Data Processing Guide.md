## NYC Annualized Sales Data Processing Guide

NYC annualized sales data was taken from the [NYC Department of Finance]('https://www1.nyc.gov/site/finance/taxes/property-annualized-sales-update.page').

Each file, from 2003 to 2018 was downloaded in excel format and converted to a csv file using Microsoft Excel.

Additionally certain adjustments were made to ready the data for import to pgAdmin.

1. delete top 3 rows
1. remove comma's from columns L-P
1. convert "SALES PRICE" column into number format and remove comma's
