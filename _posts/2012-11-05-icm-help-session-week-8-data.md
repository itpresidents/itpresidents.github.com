---
title: 'ICM Help Session Week 8: Data'
author: Mimi
layout: post
dsq_thread_id:
  - 915316690
categories:
  - ICM
---
<p>Today we mostly walked through how to get &#8220;live&#8221; data from the internet.</p>
<ul>
<li>Strings are just an array of characters</li>
<li>Operations on Strings &#8211; loadStrings(), join(), split(), match(), matchAll()</li>
<li>Basic Processing Functions &#8211; http://processing.org/reference/</li>
</ul>
<h1>Getting Data</h1>
<h2>Formats</h2>
<p>CSV: Comma Separate Files</p>
<ul>
<li>Mostly stuff you download</li>
<li>Tables, spreadsheets</li>
<li>Line breaks represents rows of data</li>
<li>For each row, column values are separate by commas</li>
<li>A lot of &#8220;static&#8221; or periodically released data comes in this format (e.g. Goverment data that&#8217;s released once a year, etc)</li>
</ul>
<p>XML: Extensible Markup Language</p>
<ul>
<li>Looks like html, data is encapsulated in between &#8220;open and close tags&#8221;</li>
<li>&lt;TITLE&gt;Beauty and the Beast&lt;/TITLE&gt;</li>
</ul>
<p>JSON: Javascript Object Notation</p>
<ul>
<li>Data format native to Javascript</li>
<li>Very user-friendly in terms of readability</li>
<li>Data stored as key-value pairs (e.g. Title: Beauty and the Beast)</li>
<li>Values can be Strings, Arrays (lists) or another Object containing key-value pairs</li>
<li>Most &#8220;live&#8221; constantly updated data is now released in JSON (e.g. Tweets, NYT, etc)</li>
</ul>
<p>If you&#8217;re wondering about how to get data, try googling, API and JSON or API and XML with the the name of the service you&#8217;re interested in.</p>
<h1>We focused mostly on JSON&#8230;</h1>
<p>Processing doesn&#8217;t know about the JSON data format. So you&#8217;ll need to use <a href="http://blog.blprnt.com/blog/blprnt/processing-json-the-new-york-times">Jer Thorpe&#8217;s library</a> to parse any JSON you get from the web.</p>
<p>Jer walks through pulling data from the NYT by using the NYT API. At a high-level, here are the main steps:</p>
<ol>
<li><a title="Get JSON LIbrary" href="http://www.blprnt.com/processing/json.zip">DONWLOAD JSON LIBRARY</a>: Put the entire &#8220;json&#8221; folder from the zip file into Processing&gt;&gt;libraries.</li>
<li><a href="http://developer.nytimes.com/apps/register">Go get yourself an API Key</a> from the NYT. (You&#8217;ll need to log in with a NYT account.) The API key is basically a big long string of letters and numbers and it&#8217;s how NYT associates the data requests you&#8217;re making with you (in case you do something bad <img src='http://itp.nyu.edu/residents/wp-includes/images/smilies/icon_wink.gif' alt=';)' class='wp-smiley' /> </li>
<li>Try running <a href="https://github.com/itpresidents/ICM-Help-Sessions/tree/master/ICM_Help_Session_Week_8">this example</a>.</li>
</ol>
<h1>Resources</h1>
<ul>
<li>Your JSON data is going to come back as one continuous string of characters. <a href="http://jsonformatter.curiousconcept.com/">Use this</a> to format it nicely with line breaks and indentation so it&#8217;s easier to read.</li>
<li><a href="http://processing.org/learning/data/">Dan&#8217;s latest write up</a> on working with text and data, updated for Processing 2.0.</li>
<li>Documentation on <a href="http://developer.nytimes.com/docs/article_search_api/">how to construct queries</a> for getting NYT data.</li>
</ul>
<h1>Where to get Data</h1>
<ul>
<li><a href="http://www.guardian.co.uk/data">The Guardian Data</a></li>
<li><a href="http://www.programmableweb.com/apis/directory/1&amp;sort=mashups"> Programmable Web</a></li>
<li><a href="http://developer.rottentomatoes.com/">Rotten Tomatoes</a></li>
<li><a href="http://developer.vimeo.com/">Vimeo</a></li>
<li><a href="https://dev.twitter.com/">Twitter</a></li>
<li><a href="http://www.flickr.com/services/api/">Flickr</a></li>
</ul>
