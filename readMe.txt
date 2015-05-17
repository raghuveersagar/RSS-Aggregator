Project Background:

What is RSS?

If you like some websites you periodically keep on checking to see something new has been updated.
So you have to keep track of all websites and visit them to check if they have any new stories.

Instead of you checking again and again it would be nice if the website told you that it has something new.
Websites have files called RSS feeds ,which the user can subscribe to, and whenever there is a new story website updates the feed file.

Aggregators:
But how do you know that feed file has been changed?So use an aggregator that periodically reads these feeds from all websites and checks whether there is anything new.Then it presents to the user all the new stories from all websites.


Project Details:
A perl script (or suite of scripts):which
reads:   "feeds" a plain text file which contains the feeds from all websites which users wishes to receive updates from.
generates:  "rss updates" an html file with the new updates and old unread entries.

General Methodology:

The feed files are in XML format.We parse the whole all feeds file and aggregate them in an html file with auto refresh enabled.Also the perl script will be run as cron job.


Make sure following 8 files are present.
1) feeds
2) logo.jpg
3) tags_generator.pl
4) rss_aggregator.sh
5) page_template
6) html_writer.pl
7) parseFeed.awk
8) helpers.pl

1.How to add a feed or subscribe to a feed:
---------------------------------------------
Add the url of feed XML in the feeds file.Also make sure feed XML id rss version2.0.
There are already 3 predefined subscriptions in the feeds file.

Also we are adding few more feedXMLs below:

http://rss.sciam.com/ScientificAmerican-Global?format=xml
http://feeds.feedburner.com/time/topstories?format=xml
http://feeds.feedburner.com/OnlineMarketingSEOBlog?format=xml

Make sure 'feeds' file has no blank lines or unwanted spaces. 


2.How to run the aggreator?
-----------------------------------

Copy all the files to a directory.Make sure *.awk,*.pl,*.sh files have execute permissions.
Then execute 'rss_aggregator.sh'.
A new file 'rss_aggregator.html' is created.


3.How to check output?
--------------------------
Please open 'chrome browser'.Go to 'File'->'Open File' .Open 'rss_aggregator.html'.  
 


