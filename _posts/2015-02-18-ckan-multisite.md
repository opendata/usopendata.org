---
layout: post
title: 'Announcing the CKAN Multisite Project'
author: waldoj
---

Today, we’re pleased to announce CKAN Multisite, a project that will make it trivial to create a new [CKAN](http://ckan.org/)-based data repository by making it easier to host CKAN sites. We’re going to drive down the cost of hosting open data, allowing states to provide open data hosting for their cities and counties, commercial hosting companies to be able to sell low-priced data hosting, and facilitate innovation in a space that is now out of reach of many organizations and governments. The minimum viable product for an open repository is not minimal enough—we think CKAN Multisite will get it there.

To make CKAN Multisite a reality, last month we published [a pair of RFPs to improve CKAN](https://usopendata.org/2015/01/07/ckan-rfp/)—one to add full data export to CKAN, one to create a Docker-based, multisite CKAN management tool—and last week we selected the winning bids from a series of _great_ proposals. We’ve awarded both contracts to [boxkite](http://www.boxkite.ca/), an Ottawa-based software development shop, so now they’re taking on the entire project.

boxkite is run by Denis Zgonjanian and Ian Ward. Denis was on the team that extended CKAN to serve as [the data repository for Canada](http://open.canada.ca/data/en/dataset), and Ian serves as the technical lead on CKAN. So they’re deeply qualified to do the work. But the biggest reason that we awarded the contracts to them is because they’re already doing some great work in this area. They’ve done a lot of work to Dockerize CKAN—that is, to make it trivial to deploy and run many sites on a single server. So now boxkite will build a management and deployment tool atop the great work they’ve already done, and add site export functionality (allowing people to leave their small CKAN site for a larger one, or to transition to [other platforms](http://how-to.usopendata.org/basics/data-repositories.html), such as ArcGIS Open Data, DKAN, Junar, OpenDataSoft, Socrata, etc.)

[The plan for this project](https://github.com/opendata/CKAN-Multisite/blob/master/Proposal%20Draft.md) was put together by the [Open Knowledge Foundation](https://okfn.org/), the indispensible organization that’s behind CKAN and so many other brilliant open data projects. (Their plan is far-reaching, beyond what we can do now—so anybody looking to make improvements to CKAN would do well to start there.)

Our development timeline has this scheduled for a late-spring v1.0 release. Of course, all work will be done [in the open, via GitHub](https://github.com/opendata/CKAN-Multisite), and all code will be published under an open source license. We’re excited about the work, grateful to have boxkite as partners in this effort, and extremely enthusiastic about what people are going to do with the resulting software.
