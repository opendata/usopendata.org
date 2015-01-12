---
layout: post
title: 'The Financial Value of Open Corporate Data to Government'
author: waldoj
---

At the U.S. Open Data Institute, we recently used government data to audit a small city’s business licenses, and we found that 30% of the city’s businesses were operating without a license. The city is losing out on somewhere between hundreds of thousands and millions of dollars of business license revenue—as much as 2% of the city’s annual budget. It’s a compelling case for the significant economic value of open data to government. This is the story of how it happened.

### Opening Virginia’s Data

The state of Virginia does not provide open data about corporations. They have [a website](https://sccefile.scc.virginia.gov/Find/Business) where people can search, one business at a time, and read some of the data that the State Corporation Commission stores about it. The only way to get a list of all 786,308 registered corporations is to [pay the SCC $450 for a three-month data subscription](http://www.scc.virginia.gov/clk/purch.aspx) and [sign a five-page contract](http://www.scc.virginia.gov/clk/files/sale.doc).

In April, I signed that contract and wrote that check, making me only [the seventh paying customer for this data](https://gist.github.com/waldoj/8836935). (Within minutes of getting access to the data, I began giving it away for free, thus preventing anybody else from having to pay for it.)

The data was a mess. It’s in no particular format, other than fixed-width ASCII, and it’s thick with inconsistencies, errors, and character encoding problems. Here’s a sample:

<script src="https://gist.github.com/waldoj/c02bfae33ae498ba451c.js"></script>

Turning this into useful data required creating [an entire software project](https://github.com/openva/crump/), which I’ve developed over the course of nights and weekends throughout the spring, summer, and fall (and is by no means finished). This package cleans up the data and transforms it into CSV and JSON.

I had [Elasticsearch](http://www.elasticsearch.org/) ingest the data (in lieu of a database), and [hacked together a website](https://vabusinesses.org/) to search the data.

This experimental, unadvertised site hadn’t been up for long when I got an e-mail from an employee of a municipal government in Virginia. She’d stumbled across the site, and hoped I could provide her with a list of every business located in her town. The reason, she explained, was that _they had no way of knowing what businesses existed within their boundaries._ The state doesn’t just withhold data from the public—they withhold it from localities, too. They had no way of knowing which businesses were failing to pay their business license fees or business property taxes.

Providing her with that data took a couple of months. That’s because the addresses in the data were wildly inconsistent, sometimes wrong, and of course not geocoded. Paying to geocode all of the records would have cost thousands of dollars, so I had to figure out how to get access to the state’s geocoder. [The state’s geodata department](http://www.vita.virginia.gov/isp/default.aspx?id=8404) was extremely helpful, and soon I had [a script geocoding all of the addresses](https://github.com/openva/crump/blob/master/geocode). I was able to send several thousand records to that municipal employee, as a spreadsheet. It remains to be seen what they’ll do with those records, if anything.

### Using Virginia’s Data in Charlottesville

Remembering that I’m acquainted with the commissioner of the revenue—the tax collector—in my home of Charlottesville, I generated the same spreadsheet for him. But his office is limited by the proprietary software that they use, and the only way for them to figure out which businesses were registered with the state and unlicensed with the city was by having a person look up each of them, one at a time, an impractical task. So they sent me spreadsheet of all 4,253 licensed businesses in Charlottesville (data that should be open, but that is not). Their records don’t use corporate identifiers, and their street addresses aren’t normalized, so I used [the Census geocoder](http://geocoding.geo.census.gov/geocoder/) to standardize the addresses and wrote some code to match up state records with city records.

The result was a spreadsheet of 1,900 businesses that list an address in Charlottesville as their place of business with the state, but that do not have a business license. That’s 30% of all Charlottesville businesses.

That does _not_ mean that there are 1,900 businesses that are breaking the law. Many of these corporations do not need to be licensed, because they don’t transact any business. Others are licensed by the state (e.g., insurance agencies), and are exempt from municipal license requirements. Some of them are businesses that are domiciled in Charlottesville, but that do all of their business in a different locality (e.g., a restaurant), and are presumably licensed in that locality. _I_ even have a corporation that’s among those 1,900, but it’s just a shell corporation—it doesn’t engage in any kind of business—and as best I know, it doesn’t require a license.

However, there are are some names on the list that I know should be licensed, but are not. How many such corporations there are remains to be seen—determining that will require a proper audit by the city’s financial staff, which they may or may not ultimately do.

The average Charlottesville business pays $1,588 in annual license fees. If all 1,900 businesses were supposed to be licensed, that would be an extra $3 million in annual income for the city, or about 2% of the city’s annual budget. If only 20% of those 1,900 are wrongly unlicensed, that’s an additional $600 thousand in annual revenue. If that estimate is right, and Charlottesville is a representative sample, then Virginia localities are collectively missing out on over $100 million each year. But these are wild estimates—again, a proper audit is required to have any real data to work with.

### Conclusions

The value of corporate registration data to localities makes it a poster child for the value of open data within government and between governments.

States should publish corporate registration data as open data, both as bulk data and as an API. By working with a representative sample of localities in the development phase, they can maximize its utility. For example, they should provided an API-based search by name, address, etc. with fuzzy matching, since many localities don’t store corporate identifiers. They should also provide a bulk service, to which a CSV file can be uploaded, which will identify the state corporate ID for each record, add the ID, and return the enriched file. And, finally, they should periodically send a spreadsheet of all corporate record changes to every municipality.

Where possible, localities should use software that stores state corporate IDs, and that provides robust import/export functionality. There is little competition in this space at present, but given the economic value of sharing this data, the market should address this on its own.

Secretaries of state should establish corporation data schemas for states to adhere to, so that vendors don’t need to accommodate fifty different standards. [The National Association of Secretaries of State](http://www.nass.org/) (NASS) is a good candidate for this. Realistically, several states should collaborate to put together a common practice first, adopt that as an informal schema, and while NASS chews on that for a couple of years, it can become the de facto standard that is eventually ratified.

I speculate that the value of this data goes well beyond local income taxes. Is Virginia's State Corporation Commission sharing corporate registration data with the Department of Taxation? Or the Department of Professional and Occupational Regulation? Or the Department of Health Professions, the Virginia Employment Commission, or the Department of Business Assistance? There are clear business cases for each of those examples, allowing the state to increase revenue and strengthen its regulatory framework without increasing taxes or passing any new laws.

It’s time to open up corporate registration data, to help government to operate more efficiently and effectively.
