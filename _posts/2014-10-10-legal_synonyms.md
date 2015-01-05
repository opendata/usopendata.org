---
layout: post
title: 'The Legal Synonyms Project: A Decent Start'
author: compleatang
---

When Waldo first asked me to look into making a synonyms file based on the context of how words are situated within a large legal corpora I thought, "Well, that should not be a problem. It seems a common situation to overcome so I am sure that there is an open source library out there. I'll just take the library and run some legal codes against it and Bob's your uncle." Turns out it was not that easy. The idea we were aiming for was fairly simple: take a large body of words, and break those down and compare the words to find where words have been used in similar contexts, because those words are probably synonyms of one another.

I began my research into the preparation of synonyms from a large corpus of documents where I would normally begin such a project: by searching GitHub. Unlike some other times, this research proved surprisingly complex. It was complex for a couple of reasons. The first was that there was not a lot of code available that had been open sourced and was meant to deal with our problem set. The second reason was that researching "synonyms" or "legal synonyms" is a bit tricky because when you perform searches there is a distinctly low ratio of signal to noise. It eventually became clear that there was not much code which was publicly available.

Once I hit a wall finding libraries that would assist my building process, I turned to academia. There is a lot of information on computational linguistics, synonym theory, and the like in journals. The challenge for me was that I'm a lawyer, not a linguist and especially not a linguist at the level required to fully comprehend the academic papers. That said, I was able to mostly piece together what the process for creating a synonyms file was. In general, from the academic research I read, there appear to be three phases to developing a synonyms file.

The first phase seeks to break the corpus into pieces and categorize the words in each of those pieces. It was important based on our design idea, that the synonyms file be built from a large corpus (e.g., a state code or the U.S. Code—which was the basis for my testing), so this required a large amount of natural language processing capability to first break down a large text file into its constituent pieces and then categorize those pieces. There was a difference of opinion as to how to break the pieces down, but categorizing them was fairly straightforward and just required a natural language processor (which is sort of like a computerized sentence diagrammer) to determine what part of speech the word was being used as.

The second phase in developing a synonyms file is to compare each of the categorized pieces of the overall text to find a similarity index between different words. This step in the process is, mathematically, where there appears to be the most debate within the academic research which I read. There appear to be many different algorithms for how to approach developing the similarity index—which is simply a number which compares two words and the relevant contexts in which they appear. When two words appear in a similar context numerous times then they would have a high similarity index and vice versa.

The third phase in developing a synonyms file is simply to pull everything out and finalize it. This was, for obvious reasons the easy bit.

We have [developed a system](https://github.com/opendata/Legal-Synonyms) which begins to automate the process. It is far from perfect, but it is a decent start. [The README for the repository](https://github.com/opendata/Legal-Synonyms/blob/master/README.md) contains some notes as to the current shortcomings of the script. They are mainly in optimization, as well as perhaps having someone more versed in computational linguistics than we are to take a look at deriving the similarity index.

So we welcome the community to dig in. The base is built, and we're hopeful that the community can use this script and help make it better.
