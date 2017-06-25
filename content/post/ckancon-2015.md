+++
categories = []
date = "2015-07-18T00:00:00Z"
description = "CKANCon 2015"
tags = []
thumbnail = ""
title = "CKANCon 2015"

+++
Michael Easter files this report from a trip to Ottawa:

[CKAN](https://en.wikipedia.org/wiki/CKAN) is a web-based, [open-source](https://github.com/ckan/ckan) data management system, maintained by the [Open Knowledge Foundation](https://en.wikipedia.org/wiki/Open_Knowledge_International). It powers many data catalogues around the world, including some heavy-hitters: [Data.gov.uk](https://data.gov.uk/about) , [Data.gov ](https://github.com/GSA/data.gov/)in the United States, and the [federal Open Data portal](http://open.canada.ca/en/open-data) in Canada.

It is primarily written in Python, using PostgresSQL to store meta-data about data sets, and Apache Solr as a search engine. CKAN is extensible via plugins, and the community takes pride in the rich set of plugins available in the CKAN ecosystem.

CKANCon 2015 was a one-day conference in Ottawa, intended both for developers and policy makers. The morning consisted of several presentations and lightning talks. A video stream of the presentations is [available here](https://www.youtube.com/watch?v=OmX-rsSYmrc) (there is a black screen early on: jump past it, using [this agenda](https://www.eventbrite.com/e/ckancon-2015-tickets-16681567016) as a guide). The afternoon featured two working groups: one technical, and one for policy / workflow.

As a newbie to CKAN, my primary goal was to become more familiar with the project. It is a terribly tired cliché, but it really is a friendly community. The developers are technically sharp, but also emit the vibe that they are entrusted with a larger, noble purpose, regarding open data. (The community reminds me of librarians in this regard.)

I was impressed with the sophisticated architecture options: e.g. the [Harvest plugin](https://github.com/ckan/ckanext-harvest) can import data from other CKAN sites into a primary site. There are plenty of other features (searching, reports, graphs, etc) to ensure that a catalog is more than “[a fancy FTP server](https://www.youtube.com/watch?v=OmX-rsSYmrc&feature=youtu.be&t=2h18s)”.

The conference ran fairly smoothly but I was surprised that there wasn’t a call to action, or a clear message on how one could contribute. The conference had [solid introductory material](https://www.youtube.com/watch?v=OmX-rsSYmrc&feature=youtu.be&t=19m55s), but was ultimately “inside baseball” (which is reasonable, if not unavoidable). A vague, secondary goal of mine was to discover an area where PEI Devs could make a difference. (One whimsical example is a Clojure wrapper around a REST API, or some such. Some nice-to-have that would add value and be of interest to our group.) Unfortunately, I waited too long to ask, and muffed the few opportunities I had.

I think an architectural tour / installation of CKAN would be a terrific talk for our group, if anyone is interested.

M. Easter