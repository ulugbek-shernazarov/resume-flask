title: Web scraping with Python
date: 2022-06-09
description: Discussing dynamic page scraping
tag: python
project: Advanced Python Course
platform: Python Practicum
link: http://example.com

Imagine that we want to scrape a platform containing public property listings. We want to get the price of a property, its address, distance, station name and the nearest type of transport to it in order to find out how property prices are distributed depending on the availability of public transport in a particular city.

Suppose the query will result in a results page that looks like this:
Search results for scraping in Python
Once we know which elements of the site store the necessary data, we need to come up with scraping logic that will allow us to get all the information we need from each ad.
We have to answer the following questions:

* How to get one data point for one property (for example, the data from the price tag in the first ad)?
* How to get all data points for one property from the whole page (eg all price tags from one page)?
* How to get all data points for one property of all results pages (eg all price tags from all results pages)?
* How to resolve the inconsistency when the data can be of different types (for example, there are some ads that have the price on request in the price field. Eventually we will have a column consisting of numeric and string values, which in our case does not allow us to analysis)?
* What is the best way to extract complex information (For example, let's say each ad contains information about public transportation, such as “0.5 miles to XY subway station”)?