---
title: 'ICM Help Session Week 8: Data'
author: Mimi
layout: post
permalink: /icm-help-session-week-8-data/
dsq_thread_id:
  - 915316690
categories:
  - ICM
---
# 

Today we mostly walked through how to get “live” data from the internet.

*   Strings are just an array of characters
*   Operations on Strings – loadStrings(), join(), split(), match(), matchAll()
*   Basic Processing Functions – http://processing.org/reference/

# Getting Data

## Formats

CSV: Comma Separate Files

*   Mostly stuff you download
*   Tables, spreadsheets
*   Line breaks represents rows of data
*   For each row, column values are separate by commas
*   A lot of “static” or periodically released data comes in this format (e.g. Goverment data that’s released once a year, etc)

XML: Extensible Markup Language

*   Looks like html, data is encapsulated in between “open and close tags”
*   Beauty and the Beast

JSON: Javascript Object Notation

*   Data format native to Javascript
*   Very user-friendly in terms of readability
*   Data stored as key-value pairs (e.g. Title: Beauty and the Beast)
*   Values can be Strings, Arrays (lists) or another Object containing key-value pairs
*   Most “live” constantly updated data is now released in JSON (e.g. Tweets, NYT, etc)

If you’re wondering about how to get data, try googling, API and JSON or API and XML with the the name of the service you’re interested in.

# We focused mostly on JSON…

Processing doesn’t know about the JSON data format. So you’ll need to use [Jer Thorpe’s library][1] to parse any JSON you get from the web.

 [1]: http://blog.blprnt.com/blog/blprnt/processing-json-the-new-york-times

Jer walks through pulling data from the NYT by using the NYT API. At a high-level, here are the main steps:

1.  [DONWLOAD JSON LIBRARY][2]: Put the entire “json” folder from the zip file into Processing>>libraries.
2.  [Go get yourself an API Key][3] from the NYT. (You’ll need to log in with a NYT account.) The API key is basically a big long string of letters and numbers and it’s how NYT associates the data requests you’re making with you (in case you do something bad ![;)][4] 
3.  Try running [this example][5].

 [2]: http://www.blprnt.com/processing/json.zip "Get JSON LIbrary"
 [3]: http://developer.nytimes.com/apps/register
 [4]: http://itp.nyu.edu/residents/wp-includes/images/smilies/icon_wink.gif
 [5]: https://github.com/itpresidents/ICM-Help-Sessions/tree/master/ICM_Help_Session_Week_8

# Resources

*   Your JSON data is going to come back as one continuous string of characters. [Use this][6] to format it nicely with line breaks and indentation so it’s easier to read.
*   [Dan’s latest write up][7] on working with text and data, updated for Processing 2.0.
*   Documentation on [how to construct queries][8] for getting NYT data.

 [6]: http://jsonformatter.curiousconcept.com/
 [7]: http://processing.org/learning/data/
 [8]: http://developer.nytimes.com/docs/article_search_api/

# Where to get Data

*   [The Guardian Data][9]
*   [ Programmable Web][10]
*   [Rotten Tomatoes][11]
*   [Vimeo][12]
*   [Twitter][13]
*   [Flickr][14]

 [9]: http://www.guardian.co.uk/data
 [10]: http://www.programmableweb.com/apis/directory/1&sort=mashups
 [11]: http://developer.rottentomatoes.com/
 [12]: http://developer.vimeo.com/
 [13]: https://dev.twitter.com/
 [14]: http://www.flickr.com/services/api/