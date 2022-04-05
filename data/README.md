# README.md

This folder contains the data sets used for the Tabluea course.

The file DECENNIALSF2010.P1_data_with_overlays_2022-03-21T154650.xlsx came from https://data.census.gov/cedsci/table?g=0400000US19%241000000&d=DEC%20Summary%20File%201
Iowa population by county 2020. This file contains county population census counts for Iowa. The data is broken into districts, so the total population for a specific county must be calculated by summing the counts for that county's districts.

Note, however, that this data contains coding that does not allow for easy processing. See the note below.

## Update

It turns out that the file noted above did not have accurate population data. To get the correct data, you must use an API call to the census website. The correct call is just using this API in a web browser: <https://api.census.gov/data/2020/dec/pl?get=NAME,P2_001N&for=county:*&in=state:*>.

Using that API call will produce a page with raw JSON data. Right-click in the page and select Save As. Change the file extension to csv and change the file type to All Files. This will save the file to your local machine as a CSV file.

The CSV file will still have the square brackets from the JSON file, so those will need to be removed. Also, the county name and the state will be combined in one text field that will need to be separated.

## The Other Files

- county_pops.xlsx : the 99 counties with their population totals
- CountyRegions.xlsx : the 99 counties with their sales regions
- sales.xlsx : sales data for each sales person for one year, divided by month
- SalesPersonRegions.xlsx : a mapping of the sales persons to their regions
