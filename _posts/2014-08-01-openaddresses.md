---
layout: post
title: 'Announcing an OpenAddresses Bounty'
author: waldoj
---

At the US Open Data Institute, we’re big fans of [OpenAddresses](http://openaddresses.io/). They’re working to piece together a address-level map of the entire world, county by county, city by city, town by town. Here in the United States, that data is often published on municipalities’ websites. (For example, see [Baltimore](https://data.baltimorecity.gov/Geographic/Parcels-Shape/jk3c-vrfy), [Albuquerque](http://www.cabq.gov/gis/geographic-information-systems-data), or [Atlanta](http://share.myfultoncountyga.us/GPDownload/FultonCounty/Tax_Parcels2013).) Stitching together this data will ultimately create a map of every addressable property in the country, as entirely open data, which is essential fuel for innovation.

Today we’re announcing a bounty for contributions to OpenAddresses. We’ll pay $10 for each new United States municipality that’s added from now through September 30. All you have to do is file a pull request [on the project’s GitHub repository](https://github.com/openaddresses/openaddresses), and the team has to accept your pull request. Come October, we’ll tally up your contributions, get in touch with you to ask about how to pay you, and then we’ll send you money. It’s that easy.

There are a few rules and restrictions. Qualifying contributions must contain `data`, `website`, `license`, `compression` (where applicable), `type`, and `note` fields, and the `note` field must provide basic information, such as whether the data provides points or polygons for each parcel, and what the name of the columns with address information are. Payments can only be made to people in countries where we can send you money legally (e.g., Cuba is probably off the table). We're capping cumulative payouts at $5,000, and we’ll provide public notice here and on the OpenAddresses repository if that cap is hit before October 1. There is no per-person minimum or maximum—we’ll send $10 for one municipality or we’ll send $1,000 for one hundred municipalities.

Ready to get started? [See the “Contributing to OpenAddresses” guide](https://github.com/openaddresses/openaddresses/blob/master/CONTRIBUTING.md) and start filing pull requests. Let’s go create a national geoparcel database.
