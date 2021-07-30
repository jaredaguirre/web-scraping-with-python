# Web Scraping with Python

Web scrapping is a technique used for extracting and indexing data from websites. Most of the search engines like Google use it in order to index and improve the search experience for users.

## The robot.txt file

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
