# Reading Notes 17  

## Articles  

### Web Scrape with Python in 4 minutes  
* [Link to Article](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)  

Web scrapping is a technique ot automatically access and extract large amounts of information from a website.  
1. Read the websites Term's and Conditions to understand how you can legally use the data.  
2. Make sure you are not downloading data at too rapid a rate because this may break the website.  

Inspect the website in order to find the relative path, link to the file we want to access for data.  
Webscrapping with Python uses the following libraries:  
```py
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

url = 'path to file'
response = request.get(url)
```

Use a library to parse the information, so BeautifulSoup can do that like this:  
`soup = BeautifulSoup(response.text, 'html.parser')`  

Then find all our a tags within:  
`soup.findAll('a')`  

This is just the beginning of webscrapping and how to get started.  


### What is Web Scraping?  
* [Link to Article](https://en.wikipedia.org/wiki/Web_scraping)  
Definition from Wikipedia: Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites. Web scraping software may access the World Wide Web directly using the Hypertext Transfer Protocol, or through a web browser. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. It is a form of copying, in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.  

## Videos  
### Track Amazon Prices  
* [Link to Video](https://www.youtube.com/watch?v=Bg9r_yLk7VY)  
Great video, great walk-through, I have seen this developer on many videos online.

## Bookmark/Skim  
* [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)  