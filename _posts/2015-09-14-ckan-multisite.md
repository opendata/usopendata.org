---
layout: post
title: 'CKAN Multisite Now Available'
author: waldo
---

Today, U.S. Open Data is happy to announce the immediate availability of [CKAN Multisite](https://github.com/datacats/ckan-multisite), a powerful new tool to launch, host, and manage dozens or even hundreds of data repository websites on a single server. [Built by DataCats](https://datacats.com/), CKAN Multisite consists of a Dockerized CKAN environment and an administrative interface to manage those Docker containers. Using CKAN Multisite, creating a new data repository takes literal _seconds_ instead of hours or days (or weeks or months).

This is the culmination of a ten-month process that began with [hiring Open Knowledge to create a draft proposal for making it easier to host multiple CKAN sites on a single server](https://usopendata.org/2014/12/08/ckan-multisite/). We put that draft RFP up on GitHub and, [with essential guidance from dozens of people](https://github.com/opendata/CKAN-Multisite/issues) from both the public and private sectors, we whittled down that draft RFP to the parts with which the community told us we could have the most impact. [We published a pair of RFPs in January](https://usopendata.org/2015/01/07/ckan-rfp/) and [awarded both contracts to DataCats](https://usopendata.org/2015/02/18/ckan-multisite/) (née boxkite). They’ve been working on this ever since, and we couldn’t be happier with their work.

### What It’s For

There are two benefits that we expect to see come of CKAN Multisite:

1. Creating more competition in the commercial data hosting space. There aren’t nearly enough vendors selling this service, in part because so much technical debt is accrued with each new client. This makes it _far_ simpler to offer this service.
1. Making it trivial to establish [regional data centers](https://usopendata.org/2015/03/25/rdc/). Governments, non-profit organizations, and universities throughout the country are creating shared data repositories for regional governments and NGOs, but they’ve found the technical and financial obstacles to be daunting. CKAN Multisite was created explicitly with them in mind.

### Fostering Competition

Not wanting to create vendor lock-in, since there are many other popular data repository packages out there, we simultaneously funded the creation of [CKAN Export](https://us-open-data.forms.fm/ckan-content-export), [which DataCats executed as an expansion of CKAN's API](https://github.com/mattleduc/ckanapi/tree/datapackage-export). This makes it possible to “dehydrate” a CKAN website, so that its contents can be imported into another CKAN server, or into commercial services like [Junar](http://junar.com/), [Socrata](http://www.socrata.com/), [ArcGIS Open Data](http://opendata.arcgis.com/), etc. (contingent on those services supporting its open format). Some sites are going to outgrow CKAN Multisite, or even CKAN, and we want to make it easy for them to change their environment to match their needs.

### Funding

CKAN Multisite was funded generously by [the John S. and James L. Knight Foundation](http://www.knightfoundation.org/) as a part of [their founding support of U.S. Open Data](http://www.knightfoundation.org/grants/201346962/). They provided the $22,400 in contracting costs, as well as the non-trivial amount of staff time that went into the process. We’re grateful to them for their essential support.
