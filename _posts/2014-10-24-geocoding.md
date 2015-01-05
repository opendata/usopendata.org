---
layout: post
title: 'Building the Open Addresses Stack'
author: waldoj
---

One type of data that's particularly in need of opening up is geodata. A lot of people have been working for a long time to improve the state of open geodata, but this is a time of particularly exciting advances for address data.

An essential component of the geodata ecosystem is “geocoding.” This is the process of turning address data into spatial coordinates. There is nothing about “742 Evergreen Terrace, Springfield IL” that actually tells us where on Earth that address is located, not without some external data to call upon.

First we have to locate Illinois, and there’s plenty of open data to do that. Then we have to locate Springfield, for which [the US Census Bureau’s National Places Gazetteer](https://www.census.gov/geo/maps-data/data/gazetteer2014.html) provides the necessary data. Then we have to find Evergreen Terrance, which is a taller order, but do-able, thanks to [OpenStreetMap's data](http://wiki.openstreetmap.org/wiki/Downloading_data). But knowing exactly where 742 is? That’s really quite difficult.

What we need is a database that gives us the latitude and longitude of addresses, including that one, something that looks like this:

```
741 | Evergreen Terrace | Springfield | IL | 39.6981 | -89.6194
742 | Evergreen Terrace | Springfield | IL | 39.6983 | -89.6197
743 | Evergreen Terrace | Springfield | IL | 39.6985 | -89.6200
```

This is known as an “address points file.” Put simply, geocoding is the act of using one of these files to automatically convert an address (742 Evergreen Terrace) into coordinates (39.6983, -89.6197).

Every geocoding service has to assemble their own data stack—they have to find their own sources of information to know where each address is physically located, and write their own software to do that work. That’s an enormous amount of work, and anybody doing that work needs to charge for access to their data in order to justify the investment of creating and maintaining it.

There are a handful of private vendors who have assembled and maintain their own address points files and geocoding services. Much of their data is built on top of the US Census Bureau’s TIGER (Topologically Integrated Geographic Encoding and Referencing) data, which isn’t very good, but it’s long served as a good start. From there, vendors draw on a variety of sources of data in order to improve their offerings. Using data from these vendors, [dozens of web-based geocoding services exist](http://geoservices.tamu.edu/Services/Geocode/OtherGeocoders/). All of them cost money, beyond some small threshold. At a small scale—geocoding dozens or hundreds of addresses—it can be free or inexpensive, but at the scale of thousands of addresses, geocoding quickly becomes an expensive proposition.

Enter open data.

Imagine if, instead of laboriously assembling collections of address geodata, it was available as open data, provided by each municipality and state. Then it would only need to be harvested, a trivial process. And imagine if, instead of writing geocoding software to use that data to match addresses to coordinates, there was open source software that could be used. Then it would be simple to create a bespoke geocoder for a project, for a government to create a geocoder for their jurisdiction, or to start a commercial geocoding service.

That’s not theoretical. That’s happening. Municipal and state GIS agencies are moving away from the model of selling access to their own geodata, having found that it’s cheaper to give it away. (Plus, if localities sell that data, it becomes hard for states to aggregate it and use it for their purposes—the for-pay data pollutes the openness of the rest of the data.)

Forward-thinking GIS officers around the country are publishing address points data. Shelby Johnson, Arkansas’ State Geographic Information Officer, maintains [a blog](http://geostor.blogspot.com/) where his staff announces each update to their statewide address points file. Johnson is the president of the [National States Geographic Information Council](http://www.nsgic.org/), and has established a model for other state GIS officers.

[The OpenAddresses project](http://openaddresses.io/) is at the fore of the open address points movement, collecting address files from government sources all around the world. They’re building up [an open collection of links and data about every address points file](https://github.com/openaddresses/openaddresses/tree/master/sources), available for anybody to do anything with.

Things are going even better on the software front, with two great open source geocoders having been released recently. [Mapzen's](https://mapzen.com/) [Pelias](https://github.com/pelias/pelias) is an Elasticsearch-powered geocoder and reverse geocoder (that is, it can provide the address closest to a given latitude and longitude), and it even bootstraps itself with TIGER, OpenStreetMap, and OpenAddresses data. And then there's [Code for America's](http://www.codeforamerica.org/) [Streetscope](http://www.codeforamerica.org/apps/streetscope/), which likewise relies on Elasticsearch. Instead of bootstrapping a whole nation's worth of data, Streetscope was created for Lexington, KY—so you only import the OpenAddresses data for the geographic region that you want to include in the geocoder.

There is a non-trivial amount of work to be done to create a completely open geocoding stack, and the remaining working is almost entirely in the realm of data collection. The OpenAddresses team is making rapid progress, with the growing open geodata movement within government is providing the fuel for that progress.

With a great deal of work by a great deal of people over the next couple of years, we should expect that most of the United States’ addresses will be available within open address points files. The cost of geocoding will rapidly approach zero, making it possible to geocode and thus make discoverable vast quantities of data that are now just structured text.
