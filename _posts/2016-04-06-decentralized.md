---
layout: post
title: 'The New Trend of Decentralized Government Data Aggregation'
author: waldoj
---

A new approach to government data sharing is emerging, and it has the potential to reshape how and why data is published openly: decentralized government data aggregation.

For years, governments were encouraged to publish open data for the benefit of the private sector. [This is a terrible incentive for government and its employees](https://usopendata.org/2014/06/06/reframe-rhetoric/), and consequently doesn’t work. Gradually, governments are starting to use their open data programs as a vector for sharing data between governments agencies (e.g., [a state agency sharing corporate records with localities to enable business tax audits](https://usopendata.org/2014/12/11/business-data/)), instead of as a mechanism to provide public data to the private sector for uncertain benefits (with associated handwaving about “apps”). This makes the data available to the public just the same, but uses a different incentive model, one based on how government actually works.

An early example of this was [the White House’s 2013 requirement that federal agencies publish public, machine-readable inventories of their data holdings](https://www.whitehouse.gov/blog/2013/05/16/introducing-project-open-data). The inventories must be published as a file named `data.json`, at the root of federal domains (e.g., [`usda.gov/data.json`](http://www.usda.gov//data.json), [`interior.gov/data.json`](https://data.doi.gov/data.json), [`commerce.gov/data.json`](https://www.commerce.gov/sites/commerce.gov/files/data.json), etc.), providing metadata about every dataset that they hold. The purpose of this was to allow [Data.gov](https://www.data.gov/) to harvest the data for the federal government’s central data repository, but the happy byproduct is that, by requiring that these inventories be published publicly, _anybody_ can have them. (Disclaimer: I was one of the creators of this standard.)

Another prominent example of this is in the [OpenAddresses](https://openaddresses.io) project—a private effort, but one that is powered by open geodata published by local and state GIS departments. By gathering up data from over 1,300 sources, the project has collected the coordinates of over 240 million addresses. Now the U.S. Department of Transportation is likely to emulate this approach, as [they plan their National Address Database](http://fedscoop.com/national-address-database). Although this is far from a done deal, decentralized aggregation is probably the only viable path to a national address database, so the odds are good. (Disclaimer: I am a volunteer for OpenAddresses. Apparently I’m a fan of decentralized government data aggregation.)

Just last month came a particularly exciting development in this emerging method of exchanging government data—[U.S. Secretary of Transportation Anthony Foxx asked every local and state transit agency to publish their route data openly](http://gis.rita.dot.gov/Transit/downloads/DearColleague.pdf). Specifically, he’s called on them to publish it in the [General Transit Feed Specification](https://developers.google.com/transit/gtfs/), on their website where anybody can download it, to be placed into the public domain:

> About half of the transit agencies in the United States, including almost all of the largest agencies, already collect this information in a common format, GTFS, and make it available either publicly through their Web site or directly to private companies. Each transit agency sets a variety of restrictive terms on the use of heir data. This information can be accessed for analytical purposes by the public, planning agencies, researchers, or Government agencies, but it must be requested on a case-by-case basis.
>
> The solution is straightforward: a national repository of voluntarily provided, public domain GTFS feed data that is compiled into a common format with data from fixed route systems.
> 
> This will form the basis for a National Transit Map. [...] It would be a service to your community and the Nation if your agency would permit DOT to collect your GTFS data from your Web site on a periodic basis so that we can incorporate your agency’s routing and schedule into the National Transit Map. [...] We will be placing the compiled information in the public domain as open data.

This is an important new vector for open data. Open data is sometimes better for government than closed data, because open data infrastructure is sometimes more advanced than closed data infrastructure.

[18F](https://18f.gov/), the U.S. digital services team, summed it up in a tweet last week:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">In a bureaucracy the size of the US government, our experience is the most effective way to make information travel is to make it public.</p>&mdash; 18F (@18F) <a href="https://twitter.com/18F/status/715578787405176832">March 31, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Government and its data are too big to share data through dedicated systems. But _open_ data scales up to the size of government and its data. Decentralized open data is a promising new vector to make that happen.
