# DataWrangler Introduction

Borrowed and adapted from the amazing [Alberto Cairo's website](http://www.thefunctionalart.com/p/instructors-guide.html).

## Get the data

* Download the [CO2 Emissions data file](https://drive.google.com/drive/folders/1g5VLC6fyMhnRFWq8jPon5QrZeSIydSuq?usp=sharing) from the course folder
  * This data is from the [World Bank's Data website](https://data.worldbank.org/)
  * Search "CO2" on the site to find the CO2 Emissions data

## DataWrangler overview

* [DataWrangler](http://vis.stanford.edu/wrangler/) is an old tool developed by researchers at Stanford University
* Available online for free but no longer supported
  * The online version only supports smaller datasheets
  * Could also use OpenRefine or Trifecta DataWrangler
* We're going to convert "wide" data to "long" data

## Wide data

* Preview the file in either Google Sheets or Excel
* The data is "wide" because the years are displayed horizontally
* The year is a variable.
  * We want the variable name to be the header in Row 1
  * And all of the values for the year should be beneath it
  * Sometimes called "wide" or "tidy" format

## Cleaning the data

* Do basic cleaning like you learned in Lecture 2
  * Delete the first 3 rows
  * Remove indicator name columns (they're identical and therefore useless)
  * Remove all commas (to avoid .csv conflicts)
  * Drop years 1960-1979
    * DataWrangler has a limit of 40 columns of data
  * Reminder: tracking changes is always a good idea

## Wrangling the Data

* Select all of your data (Cmd-A/Ctrl-A) and copy it (Cmd-V/Ctrl-V)
* Delete the sample data in DataWrangler
* Paste your data and click Wrangle
* Get DataWrangler to recognize the headers
  * Promote > Promote Row 1 to Header (+)

## Convert years to columns

* Select all of the year columns
* Select "Fold 1980, 1981... using header as a key"
* The data is now in long format
  * Year is treated as a variable and its values move down the sheet
  * We have a lot of duplicates of the country name
* Copy all of the wrangled data and paste into Sheets or Excel

