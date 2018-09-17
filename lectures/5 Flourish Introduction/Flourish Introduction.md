# Flourish intro

- Can create both static and interactive infographics

- Considered “freemium” software

- - The free version requires your data to be public

  - You can still embed your infographics

  - - Download them, etc

- Runs on HTML, CSS, and JavaScript

# Overview and templates

- You’ll need the datasets stored in our class Drive folder

- - We’ll be using data from the [Gapminder project](https://www.gapminder.org/)

  - - A study of variables that affect life span

- Create an account on [Flourish](https://flourish.studio/)

- Create a new visualization (red button)

- - Check out the tabs of the default visualizations

  - Click “Connections globe”

  - - This will load some default data to make this visualization work

    - The “data” tab at the top will show you the data that’s being used

    - - Use this view to format your data before uploading to Flourish

- If you know HTML, CSS, and JavaScript, you can make your own templates for Flourish

- - Click the “Mine” tab to create your own

# Basic world map

- Make a new visualization in Flourish

- - Select the “Map: the world” template option

- Check out the “Data” tab for the default dataset

- - There are 2 spreadsheets: shading-data and points-data

  - - The points-data requires latitude and longitude (so Flourish know where to place the data points)

  - Go back to preview

- The panels on the right allow you to customize the look of your visualization

- - Colors, borders, etc

  - Disable the points option

  - - The points-data option is now hidden from the data tab

- Import the Gapminder 2012 datasheet on the Data tab

- - Now, you need to select the correct columns

  - - Viewable in the right panel

  - Set the Region Name to column A (the countries)

  - Set the Values to the column for ChildrenPerWoman (G)

  - - Now check the preview tab

- Flourish uses a continuous color scheme to show the data

- - You can change this on the “Shading” panel

  - - Try turning off “Use continuous scale”
    - This will give you fewer colors in your map

# Animated scatter plot

- Create a new visualization

- - Choose the Scatter template

  - - A much more challenging template to use because of the number of options

- Import our own data

- - Notice that there is only one data sheet on a scatter plot
  - Import the Gapminder AllYears data

- Let’s study ChildrenPerYear and LifeExpectancy

- - Set Children to the X value
  - Set Life to the Y valus
  - Colour the data by Continent (c)
  - Clear out the Name and Size values

- The quick preview shows a negative correlation

- - Check out the preview tab - it’s sort of a mess

  - - Let’s split it the scatter by year
    - Change the name to column A (country name)
    - Change the Colour to D (region)
    - Change the Size to L (Population Total)

  - Time option lets us create a time slider

  - - Set Time to E (Year)

  - Change to the Preview tab

- If Flourish shows a mess of lines, you need to turn them off

- - Turn off the setting under “Line Styles”

- You now have a time slider at the top of your visualization

- - You can either play the animation or manually scrub back and forth
  - You can hide the giant year label under the “Time Slider” panel

# Facets and Stories

- You can subset your data on the Data tab

- - Find the “Grid of charts (facet) option

  - - Try creating facets based on the Region column (D)

- Let’s turn this into a story

- - Make sure your data visualization is saved with a title

- Create a new story

- - Your individual graphics can be slides in a story

  - Click the “Choose a visualization” button in the middle of your screen

  - - Select our scatter plot

- You could then add more slides that show different visualizations

- When you’re all done with the story, you can click “Export and Publish”

- - This will give you embed code for your website

# County level bubble map

- This will use the “CountyData” file

- - We’ll create 2 maps - one for total Clinton votes, one for Trump votes

- Create a new visualization

- - Choose “Map: US Counties”

  - The default is a color map

  - - We’re making a bubble mad

- Shading options

- - Remove land shading

- Upload data

- - Click the “points-data” tab
  - Import our “CountyData.csv” file

- Settings

- - We can skip the “Shading” options - because we disabled shading

  - Point Name: B (CountyState)

  - Check that latitude and longitude are detected correctly (C & D)

  - - Only needed for a bubble map (not a shading map)

  - Point Values: H (VoteDemocrative2016)

- Click the Preview tab

- - Change the Points “Maximum radius” so the dots are bigger
  - Change the Points color to a blue shade

- Let’s make a second map for Republican votes

- - Go back to the “Data” tab

  - Change the “Point values” setting to include another column

  - - H, I - comma separate your values

- Go back to the preview

- - Check the two tabs at the top to see the two maps

  - - The Republican map looks wrong - its bubbles are too large

    - Flourish is setting the largest bubble to 40 (or whatever you set it to)

    - - The two maps aren’t sharing a scale

    - Change “Scale points relative to” to "Maximum value in all data”