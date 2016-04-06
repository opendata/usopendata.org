---
layout: post
title: 'Opening Data While Prohibiting Using It'
author: waldoj
---

An essential part of publishing data openly is doing so under a license that allows people to use that data. _Copyrighted data isn't open data._ Those two things are mutually exclusive. Government who copyright their open data are saying “here is our data, please come use it” while also saying “you may not use this data.” Doing so means that serious users of the data will be scared off before they can put it to work.

### Findings

[Our U.S. states open data census](http://census.usopendata.org/) shows that about half of all surveyed datasets are encumbered by copyright restrictions.

Of the 356 extant, surveyed datasets, 171 (or 48%) are restricted by claims of copyright. 174 (or 49%) have no restrictions. For 11 (3%) of them, it’s unclear whether they’re copyrighted or not (e.g., the link to the copyright page is broken).

![The prior paragraph, graphed.](/img/copyright-graph.png)

### Datasets without restrictions

For those datasets without restrictions, overwhelmingly that’s because the site is silent on the matter of copyright. We tally that as consent that the data is in the public domain. Note that this is the opposite of private works, for which no statement of copyright is required. This is because works of government are generally in the public domain. ([Some states hold that they may claim copyright](http://copyright.lib.harvard.edu/states/), and some do not, with significant nuance between those two extremes.)

In rare cases, there is a direct disclaimer of copyright. For example, the datasets in [Washington D.C.’s repository](http://opendata.dc.gov/) link to [a copyright page](http://dc.gov/page/terms-and-conditions-use-district-data) that puts all data in the public domain by default:

> Unless otherwise noted, the data on the Sites is public domain and made available with a [Creative Commons CC0 1.0 Universal](http://creativecommons.org/publicdomain/zero/1.0/legalcode) dedication. In short, the District waives all rights to the data worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law. You can copy, modify, distribute, and perform the data, even for commercial purposes, all without asking permission. The District makes no warranties about the data, and disclaims liability for all uses of the data, to the fullest extent permitted by applicable law.

[D.C.’s copyright policy is imperfect](https://razor.occams.info/blog/2014/10/29/dc-updates-its-open-data-terms-of-use-round-2/), but it’s also the best effort made by any U.S. state.

### Copyrighted datasets

There are various ways in which surveyed datasets are restricted by copyright.

The most common restriction comes from agencies putting a copyright statement in their website footer, presumably placed there by website developers who added it reflexively. For example, [Puerto Rico’s population projections](http://www.jp.pr.gov/Portal_JP/Default.aspx?tabid=120) include "Junta de Planificación de Puerto Rico © 2015" ("Puerto Rico Board of Planning © 2015") at the bottom of the page. Agencies use that template for pages where data is published, without clawing back that copyright for the purpose of the data on the page.

Also common is the use of statewide website design standards and templates, in the same manner as agency templates. For example, West Virginia has "© 2016 State of West Virginia" at the bottom of all of their pages, including pages where they publish open data (e.g., [corporations](https://apps.wv.gov/SOS/BusinessEntity/), [vehicle crashes](http://www.transportation.wv.gov/DMV/Forms/Pages/Search-Results.aspx?Title=&DMVFormNumber=&DMVFormCategory=GHSP+NHTSA+Analysis+of+Crash+Data), and [state real estate](http://www.realestatedivision.wv.gov/info-by-county/Pages/default.aspx)).

Finally, some vendors claim copyright over state data that they host. For example, restaurant inspection record host [HealthSpace](https://www.healthspace.com/) claims copyright in the footer of their hosted client sites with "Copyright © 2014-2016 - HealthSpace Informatics, Inc." (e.g., [Wisconsin](http://healthspace.com/clients/wi/state/statewebportal.nsf/home.xsp), [Virginia](http://healthspace.com/Clients/VDH/VDH/web.nsf)). They probably don't mean to claim that they own these states’ restaurant inspection records, but that's exactly what they’re doing. Likewise, [Socrata](https://www.socrata.com/) claims copyright over all of their [Open Checkbook](https://opencheckbook.demo.socrata.com/) sites (e.g., [Iowa](http://checkbook.iowa.gov/#!/year/2016/)) with “© Socrata” in the footer of every page.

There are a subset of states claiming copyright over data in which they seem to be doing so deliberately. For example, Vermont's geodata site has a “[Warranty and Copyright Notice](http://vcgi.vermont.gov/sites/vcgi/files/warehouse/VCGI_Warranty_Copyright_Notice_2013.pdf)” (as a PDF, for maximum irony) that says that “certain information contained within is the intellectual property of the State of Vermont,” but doesn't specify _what_ information. They also prohibit the resale of state data and require that their copyright claims travel with the data.

### Next steps

Here are three things that governments (state and otherwise) can do to address this problem:

1. Claw back claims of copyright on data pages. If the site’s footer claims copyright, explicitly disclaim that copyright, affirmatively placing that data in the public domain (or, better, published under a [Creative Commons Zero](https://creativecommons.org/publicdomain/zero/1.0/) license—“public domain” is not meaningful to users of that data outside of the United States).
1. When publishing data within repository software, use its built-in metadata functionality to specify that the data is public domain.
1. Remove that troublesome copyright footer entirely. Just because a governments _can_ claim copyright doesn’t mean that your government needs to, over data or otherwise.

Governments have to end the practice of publishing data while simultaneously prohibiting people from doing anything with it, or risk fatally hobbling their open data efforts.
