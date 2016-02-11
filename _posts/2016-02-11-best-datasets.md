
---
layout: post
title: 'Best-of-Breed State Datasets'
author: waldo
---

Having completed [our census of U.S. states’ open data holdings](https://census.usopendata.org/), we can start studying the aggregate data and drawing some conclusions. (As, indeed, can anybody, [using the raw census data](https://docs.google.com/spreadsheets/d/1OhVbryeHBsPjJ3TjjVFlfM552pDKRjiUpTAXQJe9miA/).) First up: highlighting the very best examples of each type of dataset. We include nine types of datasets in this census, and following are the states that came out on top.

### Incarceration
Prison population data—how many people are held in each facility relative to capacity, and how that’s changed over time. [Connecticut does this best](https://data.ct.gov/Public-Safety/Correctional-Facility-Daily-Population-Count-By-Fa/n8x6-s299), earning a score of 95%. It falls short by being incomplete, because the dataset does not include the capacity of each facility.

### Legislative
Legislators and legislation—what bills are filed and who is filing them. Again [Connecticut does this best](https://www.cga.ct.gov/asp/menu/legdownload.asp), earning a score of 95%. Its shortcoming is that the legislature claims copyright over the data (with “© 2016 Connecticut General Assembly” printed in the footer), preventing people from actually doing anything with the data. (This is very common.)

### Population Projections
How the population of municipalities is forecast to change in the decades ahead. [Colorado does a perfect job at this](https://data.colorado.gov/Demographics/Colorado-Population-Projections/q5vp-adf3), earning a score of 100%.

### Real Estate
Buildings and land that are owned or leased by the government. [Oklahoma earns a perfect score](https://data.ok.gov/dataset/2015-real-property-asset-data/resource/6c1d09b3-15ba-478d-9b83-ac847adc26a3), providing detailed information about all 13,792 state holdings as CSV and via an API.

### Restaurant Inspections
The outcome of inspections of food services facilities. [New York comes out on top here](https://health.data.ny.gov/Health/Food-Service-Establishment-Last-Inspection/cnih-y5dw), with a score of 95%, but with a significant caveat: their licensing terms. All data that they publish on their repository is bound by [a confusing, restrictive license](https://data.ny.gov/download/77gx-ii52/application/pdf), ironically published as a PDF.

### Vehicle Crashes
Car accidents and detailed data about the circumstances under which they occurred. [South Dakota does an excellent job here](http://safesd.gov/raw-data.html), earning a score of 90% with their detailed, pipe-delimited bulk data. They lose points for not providing any mechanism by which the public can verify that their copy of the data is accurate (e.g., [serving it over HTTPS](https://usopendata.org/2015/11/18/https/)), and by not including the data in their data repository (because South Dakota does not have a repository).

### Companies
The state register of all companies in the state. [The state of Washington does a perfect job at this](https://www.sos.wa.gov/corps/AllData.aspx), earning a score of 100%, providing data as both tab-delimited text and as XML.

### Address Points
A list of every address in the state and its coordinates. [Washington DC does the best job here](http://opendata.dc.gov/datasets/aa514416aaf74fdc94748f1e56e7cc8a_0), earning a score of 95%. Admirably, they affirmatively place the data in the public domain. They don’t have a perfect score because it could not be determined whether the data is up-to-date.

### Checkbook
Every expenditure by the state, broken down by municipality. Again, [Connecticut does the best job](https://data.ct.gov/dataset/State-of-CT-Open-Expenditures-Ledger/4b3c-3g3a), with a score of 95% for this dataset. The only shortcoming is that there is no description for each transaction, to know what the expenditure was for, although there are multiple expense categories that allow for a good idea of the purpose.

---

There are a pair of themes that emerge here.

One is that Connecticut seems to do everything well. There were a several categories in which Connecticut did very nearly as well as the best state. So, when in doubt, emulate Connecticut.

Another is that a non-representational portion of these datasets are hosted on a data repository. Perhaps it’s just that states that have solid data holdings tend to invest in repositories, but hosting a dataset in a repository often has the effect of increasing its score. That’s because repository software tends to encourage—or can even force—better practices. For instance, [Socrata](https://www.socrata.com/)’s repository software uses HTTPS by default, guaranteeing that the data is verifiable (worth 5% of the score), and ensures that that machine-readable data is also available in bulk (worth another 5%). Because repository software offers no mechanism for the sale of data, the presence of a dataset within it ensures that it is without cost (another 5%). And, of course, a dataset being a repository is itself worth 5%. So the act of putting a dataset in modern repository software yields a 20% score increase. The lesson here is to establish a repository because doing so encourages good practices.
