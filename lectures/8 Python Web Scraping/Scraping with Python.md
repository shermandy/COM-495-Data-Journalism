# Scraping with Python

## Setup

You'll need to have Python installed on your computer to follow these steps. If you have a Mac, you're good to go! It's already included. If you have a Windows computer, you need to [download it from Python's website](https://www.python.org/downloads/).

Once you have it installed, open a terminal window and type the following to check the version number of Python.

```
python -V
```

If you get an error, the install failed. If it worked, you should see a version number like 2.7.10.

Next, you need to the libraries we'll use to help scrape a website. Run the following two commands in your terminal.

```
pip install BeautifulSoup4
pip install requests
```

Note: if these fail, you may need to add `sudo` before each line. `sudo` will require your computer's password. It's your way of authenticating yourself and giving the terminal permission to install the libraries.

## Importing the required libraries

Add the following code to a new .py document

```python
from bs4 import BeautifulSoup 
import requests

link = requests.get('http://quotes.toscrape.com/')

soup = BeautifulSoup(link.text, 'html.parser')

print(soup)
```

Run the code in your Terminal window. You should see the entire webpage code printed in the terminal.

Delete the `print(soup)` line so it won't be printed any more

## Search for the needed HTML elements

Let's search for the container that wraps around each quote. Use the inspector in your browser to find the class name. In this case, it's a `<div>` with a `class` of `quote`.

Add this code to find every instance of `<div class="quote">`

```python
results = soup.find_all('div', attrs={'class':'quote'})
```

Print the variable we just created and launch the .py script in your Terminal.

```python
print(results)
```

Inside of each `<div class="quote">` is the quote text, the quote author, and the quote's tags. Let's extract that data into newly created variables. For this website, the structure is the same for every instance of `<div class="quote">` but that's not the case for every website.

Because the structure is the same for each instance, we can, again, use `find_all` to loop through the elements.

Delete the `print(results)` so it doesn't run again.

Let's create an empty array that we can place our scraped data into. We'll add names for the header row too so they appear on row 1 in our .csv file.

```python
quotes = []
quotes.append(['Quote', 'Author'])
print(quotes)
```

Add this code and execute the script in your terminal.

Delete the `print(quotes)` if it worked.

The next step is to loop over the results, process the data, and add the good data to our `quotes` array.

We'll use a `for` loop to achieve this

```python
for result in results:
    quote = result.find('span', attrs={'class':'text'}).text.encode('utf-8')
    author = result.find('small', attrs={'class':'author'}).text.encode('utf-8')
    date = datetime.now()
    quotes.append([quote, author, date])
```

Since we are using the `datetime` function, we need to include the appropriate library at the top of the file with the other imports.

```python
from datetime import datetime
```

Print the quotes array to see if it worked: `print(quotes)`

## Outputting to a CSV file

Printing into the terminal is fine but it's not easily usable. Python can write directly to a .csv file using the css library.

Add these lines to the top of your code with the other imports:

```python
import csv
```

And finally, add this code to output the quotes to a .csv file:

```python
with open('output.csv','a') as csv_file:
    csv_output = csv.writer(csv_file)
    csv_output.writerows(quotes)
```

## Try it on your own

Choose a page from the [Texas Department of Criminal Justice page](https://www.tdcj.state.tx.us/death_row/index.html) and scrape the data.