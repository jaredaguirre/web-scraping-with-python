# Web Scraping with Python

Web scrapping is a technique used for extracting and indexing data from websites. Most of the search engines like Google use it in order to index and improve the search experience for users.

## The robots.txt file

This is just a text file that most of the webpages use in order to notify the user-agents and bots which paths they should not extract data from. This is an example from the lds.org site:

If I search on internet 'lds.org/robot.txt' you get the following:

```
User-agent: *
Disallow: /centerpiece
Disallow: /centerpiece-test
Disallow: /China?lang=cmn-hans
Disallow: /China?lang=cmn-hant
Disallow: /China?lang=cmn-Hans
Disallow: /China?lang=cmn-Hant
Disallow: /donations
Disallow: /feedback
Disallow: /institutes/calendar
Disallow: /languages
Disallow: /placestovisit/location/drive
Disallow: /scriptures/search
Disallow: /search
Disallow: /secure/email
Disallow: /services/platform
Disallow: /share-study
Disallow: /study/manual/handbook-1-stake-presidents-and-bishops
Disallow: /tools/feedback
Disallow: /youth/learn
Disallow: /comeuntochrist/*/internal-use-only/
Disallow: /comeuntochrist/*/search-results/
Disallow: /comeuntochrist/lp/
Disallow: /comeuntochrist/teach/
Sitemap: https://www.churchofjesuschrist.org/sitemaps
```

'User-agent: \*' means that all the subsequent lines apply for every user-agent or user.
'Disallow: /blabla' means that the path is not allowed for indexing or scraping. 
'Allow: /blabla/hello' means that although the root dir 'blabla' is not allowed, the 'hello' path actually is.


## An example as introduction

[requests](https://docs.python-requests.org/en/master/user/quickstart/#make-a-request) and [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#quick-start) are the main libraries for this kind of scripts

```python
import requests
from bs4 import BeautifulSoup

r = requests.get('https://www.lipsum.com/')
html_content = r.text
soup = BeautifulSoup(html_content, 'html.parser') # This is the Beautiful object necessary to parse all the data
```


