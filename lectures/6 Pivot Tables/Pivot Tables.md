# Pivot Tables

## Helpful links

* [Excel Campus, Pivot Tables - Pt. 1](https://www.youtube.com/watch?v=9NUjHBNWe9M)
* [Excel Campus, Pivot Tables - Pt. 2](https://www.youtube.com/watch?v=g530cnFfk8Y)
* [Excel Campus, Pivot Tables - Pt. 3](https://www.youtube.com/watch?v=FyggutiBKvU&t=779s)

## Introduction

* Allows you to take complex data and present it however you choose
  * Only for basic analysis
  * Built into Excel and Google Sheets
* You need to have clean data (no missing values)
  * You also need a header row
  * Can't have any blank headers, merged cells, or blank date
* In Excel, Insert > Pivot Table
  * Make sure it's selecting the entire range of data
  * Send the Pivot Table to a new worksheet in the same file

## Creating the first Pivot Table

* Drag your first variable to the "Rows" section of the Pivot Table fields (example from PA Crash Data: Weather variable)
  * Drag the second variable to the "Values" section (example: injuries or fatalities)
* The values section will automatically SUM the values the match the first variable
  * In our case, it SUMs every injury that occurred in each weather scenario
* You sort the values area
  * Right-click on any of the values > Sort > Highest to Lowest
* Creating Pivot chart
  * Analyze tab > PivotChart
  * Choose a Bar chart
  * You can then customize this chart to clean it up

## Making a new Pivot Table

* Duplicate the existing Pivot Table worksheet
* Try making a chart that shows number of accidents by county name
  * Sort it to find out which has the most/least
* You can also click the small filter icon in the Pivot Tables header row for more options
  * For example, choose Value Filters > Top 10
* You can see the columns as a percentage of the total as well
  * Add the second variable (injuries or fatalities) to the "Values" as a duplicate
  * Right-click somewhere in this column
    * Value FIeld Settings
    * Show Values As: % of Grand Total
* Try adding an additional variable to the "Rows"
  * Example: Weather

## Simplifying the presentation of data

* You can add variables as a "Filter" variable
  * Allows you to update the data based on the value of any one variable
  * Simply drag your filtering variable to the "Filters" section
* Make a new Pivot Table
  * Add the time of the crash to the "Rows" section
  * Choose your second vairable and drag it to the "Values" section
* The time of crash variable has far too many options
  * Let's create categories to make this more useable
* Analyze > Group Field
  * This lets you group the data into chunks
  * 0000 to 24000
    * Divide by every 400
* You could also add the time variable to the "Values" section to see which time category has the most injuries/fatalities (make sure this column is set to do a count of the variable - not a SUM)

## Presenting the data

* Insert another new worksheet
* Copy all of the other sheets charts and paste them into the new dashboard sheet
* Add a slider
  * Select a chart
  * Insert > Slicer
    * Choose field variables that will act as a filters
    * Example: weather
* Right click the slicer
  * Report connections
  * Select all
    * Now every chart will update when you make a selection