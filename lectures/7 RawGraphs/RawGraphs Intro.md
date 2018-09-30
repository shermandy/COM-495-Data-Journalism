## RawGraphs Introduction

* Sometimes just called Raw
* We will use two files (from course Google Drive)
  * CO2 Emission file for 2012
  * CO2 Emission file for 1980 - 2012
* Designed for both journalists and designers
  * Therefore, it has a very simple interface
* Does not create interactive visualizations

## Helpful links

* [Official RawGraphs Learning page](http://rawgraphs.io/learning/)

## Loading data and creating a scatter plot

* Load the [RawGraphs app](http://app.rawgraphs.io/)
* Load the 2012 CO2 emissions data file by copying and pasting it into RawGraphs
  * Wait until you see that it's been successfully parses
  * You could also upload a .csv file instead
* Scroll down to see the many options available in RawGraphs
  * Many are very hard to illustrate in Illustrator or a similar vector program
  * RawGraphs will allow us to create them and then export them for use in Illustrator
* By defauly, RawGraphs selects "ScatterPlot"
  * Make sure it's still selected
* Scroll down to select the variables
  * You can drag them from the green menu on the left and drop them onto the correct box on the right
  * Set the x axis to GDP per capita
  * Set the y axis to CO2 emissions per capita in tons
  * A preview should appear automatically
* We need to fix the obvious problems with the chart
  * The size of the bubbles, for example
  * Change the max radius to 3, for example
* You can also size the bubbles by another variable
  * For example, drag population to the size box
  * The preview should update
* Drag continent to the color box
  * Now each bubbles is colord by its continent
* Try dragging the country name variable to the label box
  * It's helpful but it's a mess (don't leave all of them in your final infographic)

## Pie Charts and Tree Maps

* Using the same data set as before (it's already loaded)
* Select the "Sunburst" template
  * Drag the continent to the "hierarchy" box
  * Drag the mapped variable to the "size" box
    * For example, drag "population" onto it
    * Now, the size of the segments represents the population sorted by continent
  * Add "continent" to the color box
    * We should manually merge some of these continent options
  * The sunburst is already labeled so you can leave that box empty
* A sunburst graphic is a nested pie chart
  * Can have multiple rings
  * Add the "country name" right beneath "continent" in the hierarchy box
  * You will now see each individual country organized by continent
    * But this infographic is obviously a mess
    * Avoid so many subdivisions in a pie chart
* Let's try a treemap - select it from the templates
  * Add "continent" to the hierarchy box
  * Add "population" to the size box
  * Color it by "continent"
* A tree map is similar to a pie chart - the size of the rectangels are proportional to the variable selected
  * Size of population, in this case
  * A tree map makes it easier to compare segments, especially when there are more than a few subdivisions
* We can also subdivide these chunks
  * Drop "country name" into the hierarchy box (at the bottom - beneath continent)
  * It's a mess and needs more cleaning
* You can export this as .svg at the bottom of the page

## Bubble charts

* Let's try a circle packing (which is a bubble chart)
  * We're going to recreate [something like this](https://visual.ly/community/infographic/environment/global-emissions-kyoto) chart from the Guardian
* Continent -> Hierarchy
* CO2kt -> Size
* Continent -> Color
* Preview the visualization
* Add "country" to the bottom of the hierarchy
* On the Guardian's page, the bubbles are sorted geographically (to roughly look like the world map)
  * We would need to do this manually in Illustrator

## Bump charts and area charts

* We'll now use the other data sheet - that contains the years from 1980-2013 (per country)
  * This is obviously a much larger data sheet
* Load the other data sheet into RawGraphs
  * Reload the page to start with a new data sheet
  * Give it some time to load because of the file size (wait until the green confirmation text)
    * Everything takes longer to process
  * Leave the template set to "Scatter Plot" for now
* Add "GDP per capita" to X axis
* Add "CO2 per capita" to Y axis
  * This will make a mess of a scatter plot
  * Each country appears many times on the chart (once for each year)
  * Therefore, a scatter plot is not useful in the case
    * Neither is a bar graph or other similar graphs
* Let's try a bump chart (it supports the time component)
  * Continent -> Group
  * Year -> Date
  * CO2kt -> Size
  * Preview your bump chart
    * This shows your a total sum of all CO2 emissions for each year
    * And it shows you which continent is responsible each year
    * The order of the colors also shows the ranks of each continent
    * Notice how effective this is at telling a story
  * Try adding "Country" to "Group"
    * You can't subdivide like we could with other types of charts
* Area graph - similar to the bump chart
  * Do the same variables that we just did to see the different output format

* Alluvial diagram
  * Try making an alluvial diagram with the sample dataset included with RawGraphs about Titantic passengers