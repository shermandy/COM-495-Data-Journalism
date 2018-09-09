## InZight Introduction

Borrowed and adapted from the amazing [Alberto Cairo's website](http://www.thefunctionalart.com/p/instructors-guide.html).

## Get the data

* Download the county level data file from the course Drive folder
* One file has many sheets
  * Use this to explore the data and understand the abbreviations
* The other file is only the data (cleaned up by Alberto Cairo)
  * Use this file in InZight

## Why InZight?

* Free
* Flexible
* Can explore your data and generate infographics that can be exported to Illustrator
* Two different version - one that's installed to your computer - another that runs in a browser
  * This lesson will use the browser version
  * Be ready for it to crash at times

## Getting started with InZight

* Load [InZight Lite](https://www.stat.auckland.ac.nz/~wild/iNZight/) > File > Import spreadsheet
  * Select the data-only file
* InZight allows you to preview the data but it's no better than Excel/Sheets for this
* Use the Visualize tab
* Change the first variable to something that interests you
  * Income per Capita (C.Income.Capita)
  * This will load a distribution chart with a lot of individual dots
* Click the summary tab to see overview statistics for the selected variable
  * Mean, median, max, min, quartiles
* Manipulate variables > Create variables
  * This allows you to see the summary stats of every variable quickly
  * Switch back to the visualize tab

## Histograms and Box Plots

* The default chart shows you the spread of the data
* Change it to a histogram (to avoid the mass of dots)
  * Dots are good for outliers but not much else
* Click "Add to Plot"
  * Change "Plot Type" to "histogram"
* What does this chart mean?
  * X axis vs y axis
  * Where is the mean?
  * Normal distribution?
  * Quartiles description

## Comparing Distributions & Exporting

* Subset by (under "Select Variables" tab)
  * Select "region"
  * You will be given 6 distributions - one for each US region
  * Allows for quick comparison of distribution
* Try changing it to "State"
  * 50 distributions appear - too many
  * You should download the file and use it in another program that allows you to zoom
    * Try exporting it as a PDF
* The "Summary" tab shows you the summaries of each subset
  * Very helpful for quick analysis
* Remove the subset

## Scatter plots

* Make sure you've removed the subset

### Comparing multiple variables

* Select second variable - choose "C.College 2014"
  * The percent of college graduates in the county
  * Notice the unique outliers
* This data shows a positive relationship
  * What does that mean?
  * What is a negative relationship?
    * What variables do you think would show a negative relationship?
* You can plot the linear relatioship directly
  * Click "Add to Plot" and change the menu to "Trend Lints & Curves"
    * Turn on the "linear" option to see a line of best fit

## Coloring by variable

* Sometimes it helps to highlight each data point with color
  * InZight allows you to apply color based on a variable
* Click "Add to Plot"
  * Change the menu to "Customize Plot Appearance"
  * Click "Point color" and customize your settings
    * "Color by" is the important step
* Color by state - pretty useless because 50 colors is too many
* Color by region - better example for this data
* Subset the data by region
  * Makes the color useless but shows you how the setting is applied

## Exploring correlations

* Remove the subset
* Remove the coloring
* Remove the line of best fit
* Change the variables to explore the data
  * Try comparing "Obesity Rate" to "College Degrees"
    * This is a negative example
  * Try "Poverty rate" and an ethnicity
* Remember, you are NOT seeing causation - only correlation

## Mapping with InZight

* InZight is not a mapping tool but you can do neat things with the data
* Set the variables to Latitutude and Longitude
  * You should see a rough map of the US
* Go to "Add to Plot" and change the menu to "Customize Plot Appearance"
  * Color the points by a variable of interest - try "C. Hispanic"
  * This will show you a concentration map of hispanic population
* Make the dots smaller in the InZight settings
  * You can also tweak the colors
* Try this trick with other variables
  * Some are useless but many are very interesting

## Exploring by sorting data

* Go to the "Dataset" menu and choose "Sort data by variables"
* Try finding the northern-most county
  * Sort by latitude
  * What's the southern-most county?
* What county has the highest income per capita?
  * The lowest?

## Creating new variables

* InZight also allows you to add new variables that don't already exist
  * It is clunky, however
* Go to "Manipulate variables" and choose "create variables"
* Give your new variable a name beneath "variable name"
  * Let's add hispanic, black, and asian populations
  * Select the first variable from the dropdown menu
  * Then click the + button and choose the next variable
  * Make sure the expression is outputting correctly
    * If it is wrong, you have to press the "Del" button to delete
  * When the expression is good, click "Create variable"
    * It will appear at the end of the display of all summaries
* You can also create variables based off of numerical data
  * For example, make a new variable that shows how much each county departs from the median income per capita ($22,905)
  * The expression will be "22905-C.Income.Capita"