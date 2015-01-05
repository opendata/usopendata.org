---
layout: post
title: 'Let’s Reframe Open Data Rhetoric'
author: waldoj
---

The arguments that persuade the public to support open data can be actively harmful when used to persuade government employees to support open data. We need to reframe how we describe the benefits of open data within government by understanding and accommodating the needs of the people who comprise our governments.

## This Isn’t Working

There are two arguments that are often used in favor of open data:

1. “We, the taxpayers, have paid for this data to be generated and stored, and we have a right to have it.”
2. “A democratic government has an obligation to be transparent. In the 21st century, that means providing open data.”

These arguments tend to be persusive to citizens and elected officials. I often use both of these arguments. But there's an important group to whom they're not persuasive: government employees. The people who actually open data. Imagine how you‘d feel if somebody marched into your office and told you that you needed to do something unfamiliar, confusing, fraught, and not in your job description, *because you owe it to her if you love America.* You'd probably gin up a reason not to do it.

Government employees are rational actors. They have a job to do, and “open data” appears in the job description of maybe a few dozen of them. In an economy in recovery, government agencies are short on staff and on funding—dedicating time and money to tossing data into the ether in hopes that somebody will do something useful with it...well, that’s not very sensible. We need to emphasize reality-based reasons why governments should produce open data.

## Let’s Try This

Government agencies frequently need to exchange data with other government agencies and between departments within the same agency. Local agencies communicate with their state counterparts, state agencies exchange data with other state agencies, federal government needs to aggregate data from state governments, and so on. The [Microsoft SharePoint](http://office.microsoft.com/en-us/sharepoint/) document management system is widely used in state and large municipal government, and it provides several methods of sharing data with third parties. Sometimes there might be a shared server used within a single government, with the data perhaps found on the `L:` drive in the form of an Access database. But in thousands of municipal governments and state agencies, data is shared by simply e-mailing around Excel files. (Or, often, by walking down the hall and knocking on the door of the person who has the file.) More modern agencies might use Google Docs or a similar cloud-based service, and share access to spreadsheets there. Because of these varying practices, a single state agency may well receive data in a different fashion from each of dozens or hundreds of municipalities.

This presents an opportunity for open data. If the staff list is simply a spreadsheet on a website, the real benefit of open data to government might be that Jim from HR won't have to send the same e-mail every other Friday, asking for any changes in staffing—he can just download the spreadsheet. This simplifies things for both for Jim and for the people in 20 different agencies who are tired of getting the same request from Jim every week.

There are a lot of efficiencies waiting to be realized based on intra- and inter-governmental open data. Many municipal agencies have a state counterpart. Many state agencies have a federal counterpart. Agencies collaborate with other agencies within the same government. Divisions of large agencies need to share data. And data needs move between all of these, as indeed it does, but often it does so awkwardly, at best. A non-trivial portion of agency IT departments’ work is to facilitate sharing data. 

When confidentiality isn't at issue, sharing governmental data in the open using a common protocol (HTTP) and a common format (CSV, JSON, XML, GeoJSON, etc.) can increase intra- and intergovernmental access to that data, provide more tools for producing and consuming that data, and has the happy side-effect of emitting open data for the benefit of the public.

## Results So Far

I’ve only been talking about this for about a couple of months, but it seems to resonate with audiences. When giving a talk in which I propose thinking of open government data in these terms, I can tell who works for government, because their eyes light up, they nod vigorously, and then they all come up and talk to me when I’m done. I have adopted this new tack in the course of advising state and local governments, and I've seen how it changes the minds of the holdouts at the table.

This is just one attempt to describe the benefits of open data to government employees. There are certainly others (e.g., reducing the volume of FOIA requests), any number of which might prove to be more compelling to bureaucrats than simplifying internal data sharing. The important thing is that, when pitching open data to government, we start to frame it in terms of how it will benefit them—how it will make their lives easier or contribute to their professional success—instead of framing in terms of what *we* want, or how it will benefit unidentified third parties.