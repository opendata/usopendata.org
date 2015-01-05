---
layout: post
title: 'CKAN Multisite Draft Proposal'
author: waldoj
---

We want to make it much easier for governments to create and host open data repositories. To that end we’re proposing [a “CKAN Multisite” project](https://github.com/opendata/CKAN-Multisite/), to make it easy to centralize dozens or hundreds of CKAN sites on a single server, driving the cost of an individual repository towards free. We hired the [Open Knowledge Foundation](okfn.org)—the creators of [the CKAN data repository software](http://ckan.org/)—to consider our half-baked concept and turn it into a series of actionable proposals. [Their draft proposal is now available as Markdown](https://github.com/opendata/CKAN-Multisite/blob/master/Proposal%20Draft.md) and [as a PDF](https://github.com/opendata/CKAN-Multisite/blob/master/Proposal%20Draft.pdf?raw=true).

We’d like feedback about this throughout the week, before we break up these tasks into components, issue RFPs, and award contracts to begin the work. We’d like to hear from CKAN experts about which components of this should be bid out collectively versus broken up, and about which of these enhancements best advance other goals, even if those goals are unrelated to our project. We’d like to hear from operators of open data repositories about how we can improve on this proposal to better serve their needs. We’d like to hear from people in government about whether this would help make it easier for them to publish data. And, of course, from _anybody_ who has ideas about how to improve on this.

Naturally, [we have a GitHub repository for this project](https://github.com/opendata/CKAN-Multisite/), and feedback is best provided there. (Or, if you prefer privacy, they can be sent [to me via e-mail](mailto:waldo@usodi.org).)

<center>• • •</center>

Here’s the motivation behind this project.

When somebody in government wants to publish data, there’s a yawning chasm between that desire and their _ability_ to do so. That chasm can only be bridged with time or money. (There are [a few free hosting options](http://how-to.usodi.org/basics/data-repositories.html#free-hosting), so this is improving.) I posit that if a government employee could set up a data repository with no money, a minimal amount of time, and no contract to be signed, we’d see a lot more data being opened up, especially at the state and municipal level.

Back in July, [I wrote that we need to make it trivial to deploy a new instance of CKAN](https://github.com/opendata/Open-Data-Needs/issues/5), the [popular open-source data repository software](http://ckan.org/). CKAN is famously difficult to install and configure under anything other than ideal circumstances. It seemed like it would make sense to create a master CKAN hosting service, where many CKAN instances could live. State governments could use it to provide free hosting to its agencies or municipalities, or metropolitan planning organizations could use it to provide hosting of planning data. Hosting companies could use it to provide low-cost data repository hosting. There are dozens of applications.

Right now, running dozens of CKAN instances would be laborious and expensive. Each would need its own server (if virtualized), and require security updates and maintenance.

But, with some improvements to CKAN, the required server resources could be made quite minimal, costing only a few dollars a month per site. Standing up a new site could be automated entirely. That gap between desire and ability could be reduced to the time it takes to fill out a registration form and pressing "Submit."

Why do this with CKAN? Because, of [all of the open source data repository packages](http://how-to.usodi.org/basics/data-repositories.html#open-source-software), CKAN is the most robust and the most popular. Commercial software is out of the question, of course, because without access to the source code, we can’t make improvements to it.

We’re breaking these improvements up into pieces, rather than making a monolithic project out of it. That’s because it may well fail. There may be a reason why this won’t work in CKAN, something that we haven’t seen yet. Maybe we’ll get hung up on technical problems that we can’t resolve. Maybe it’ll cost way more than we thought, and we’ll run out of money. So rather than make a monolithic improvement to CKAN, we want to make a series of small ones, each one of which will make it easier to start a new open data repository. The whole will be greater than the sum of its parts, but the parts won’t be too shabby either.

Please take a few minutes to read [the draft proposal](https://github.com/opendata/CKAN-Multisite/blob/master/Proposal%20Draft.md), and let me know if you have any thoughts about how to improve it before we get to work.
