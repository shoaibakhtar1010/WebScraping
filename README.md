# WebScraping

## 1. Extracting all data in the table

Now that you've seen how we went about extracting the trs value, see if you can extract all
of the values contained within that table, starting at Previous Close and ending at 1y Target
Est.

## 2. Wikipedia table scrap
Our next goal is going to be to scrap all the data from the yahoo finance for a list of 505
companies that are part of the S&P 500 index.
To do this we first need to know what all of these companies are and what their ticker symbol is.
In this exercise please write a webscraper that gets the ticker symbol (called Symbol in the
table) from the Wikipedia entry on the S&P 500 companies.


## 3. Combining two data sources

Now that we have created a webscrap to get a list of company ticker symbols and we also have
a webscrap to get more financial information for them from the Yahoo Finance website, it’s
time to combine these information sources.
Modify the programs we’ve created in the previous lecture to have a program that scraps
the list of S&P 500 companies for the ticker symbols, and gets the additional information from
the Yahoo Finance website.
Furthermore, put this data into a pandas dataframe (in whatever format you think is
good/appropriate for further analysis) and save it to a csv file.
Challenge:
Make this webscrap run every 15 seconds, and make sure to not overwrite your previous data file.
1. You can use the time module to get the current time and also have your program wait
for a specific amount of time
(a) You can use time.time() to get the current epoch time
(b) You can store time.time() in a variable to keep track of the time that an event
occurred and reference it later (or subtract it from calling time.time() again to get
the time difference between the event and now)
(c) You can use time.sleep(seconds) to make your program wait for a specific number of
seconds
2. You can use the os module to check if a specific file exists
(a) You can use os.path.isfile(pathToFile) to check if the file at the location referenced
in pathToFile exists.
E.g. os.path.isfile(”test/rt.txt”) checks if the file rt.txt exists in the folder test (relative to the folder where the program is saved).
3. Also use the datetime module an create an extra column that keeps track of the time the
information was recorded
(a) You can use datetime.datetime.now() to get the current date and time
(b) You can use the .timestamp() on a datetime object to get the epoch timestamp
(e.g.datetime.datetime.now() gives the current datetime’s epoch time)
