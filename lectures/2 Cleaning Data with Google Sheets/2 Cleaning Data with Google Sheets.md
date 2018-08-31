# Cleaning data with Google Sheets
* https://learno.net/courses/cleaning-data-in-excel
* [Download the .csv file](reactors.csv)

## Importing vs opening
* Always check the encoding of the file
* Use Unicode UTF-8 for most documents from web
* Make a new Google Sheets doc
	* File > Open > Upload the .csv
	* Double check the odd characters to make sure Sheets is reading the encoding correctly
## Check for errors
* What are the obvious errors with the data?
	* Do a quick scan for obvious errors
	* Be sure that each column is expanded so the text is completely visible
	* Verify that you have the correct number of entries (this file has 671)
## Blank dates
* Why are some of the "Connection" data entries empty?
	* Notice that Sheets auto recognizes the date format
# Using Data Filters
* Date > Create a filter
* Click the filter icon at the top of the Connection column (column J)
	* You can use the popup to hide non-blank dates
	* Now that you only see the blanks, what do you notice?
* Check the filter for Column 1	
	* It can be deleted - it's all the same link
	* Never delete content without saving an original copy
	* Right-click the tab for the current sheet and make a copy into the same file
	* File > Version Control (to track changes)
* Delete the first column
# Check the country column
* Click the filter icon for this column and check for obvious errors
	* What's wrong with the 'Russia 11MWe' line?
		* Fix the issue
	* Look at the Ukraine entries
	* What's wrong with the USA entries?

# Capacity column
* Why is there one 'FALSE' entry?
	* Check the source data (the source has the problem)
	* Can you delete this record?

# Formatting data
* Begin with the data column
	* Format it so it's YYYY-MM-DD
* Extract the year from the data so it's in its own column
* Make a new copy of the sheet before using formulas
* Insert > Function > Date > Year
* General equation explanation

# Status column consistency
Fixing the capitalization
* Add a column next to the Status column
* =PROPER function
	* reference the source data - not the current sheet
* Paste only the values over the capitalized entries
# Capacity
* Some have commas, some have dots, some are GWe, some are MWe
	* You need consistency
* Get rid of the dot	
	* Select just the one colum
	* Edit > Find and Replace
* Split the Number and the "MWe" into columns
	* Data > Split Text to Columns
* Converting GWe to MWe
	* Add another new column
	* Use IF statement to only convert the GWe data
	* Filter so only the GWe appear 
* Keep only the values of this formula 

# Sorting
* Apply a filter on the new capacity column
	* Sort Z > A

# Charting the data
* Insert > Chart

# Reactors vs Power Plants
* Plants with multiple reactors are listed multiple times
	* What if you want to compare the power of plants and not just reactors?
* Add a new column after A:A
	* =RIGHT(A2,1)
* Add another new column
	* =ISNUMBER(B2)
	* Why is every result 'FALSE'?
* Add *another* new column
	* =VALUE(B2)
* Update the column with all of the 'FALSE' entries to use the newest column
	* Make sure these equations are filled all the way down
* Notice how 'Bruce 1' isn't working properly
	* Why?
* Change the RIGHT formula to include a TRIM
	* =RIGHT(TRIM(A2),1)
* One more column
	* =IF(D2,C2,"")
* Just kidding, one more column
	* Name it "Reactor Names"
	* =IF(D2,LEFT(A2,LEN(A2)-2), A2)
* Copy and paste only the values in their place (no more formula)
* Delete the data that's no longer needed
	* Only need to keep these 2 new columns
# Your first pivot table
* Select all of the data
	* Data > Pivot Table
	* Rows = Power Plant Name
	* Values = Our capacity column
		* Make sure it's set to SUM
	* Under the 'Power Plant Name' option of the pivot table
		* Set sort by to "SUM of Capacity MWe" - DESCENDING
* So what power plant is the most powerful?  