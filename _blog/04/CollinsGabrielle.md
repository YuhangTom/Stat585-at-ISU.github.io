---
author: "Gabrielle Collins"
title: "Research skills"
layout: post
topic: "04"
short-topic: "Ethics and Reproducibility..."
due-date: 2022-02-17
root: ../../
---


## Prompt:

In May 2015 Science retracted - without consent of the lead author - a paper on  how canvassers can sway people's opinions about gay marriage, 
see also: http://www.sciencemag.org/news/2015/05/science-retracts-gay-marriage-paper-without-agreement-lead-author-lacour
The Science Editor-in-Chief cited as reasons for the retraction that the original survey data was not made available for independent reproduction of results, that survey incentives were misrepresented and that statements made about sponsorships turned out to be incorrect.<br>
The investigation resulting in the retraction was triggered by two  Berkeley grad students who attempted to replicate the study and discovered that the data must have been faked.
 
[FiveThirtyEight](https://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/) has published an article with more details on the two Berkeley students' work.

Malicious changes to the data such as in the LaCour case are hard to prevent, but more rigorous checks should be built into the scientific publishing system. All too often papers have to be retracted for unintended reasons. [Retraction Watch](https://retractionwatch.com/) is a data base that keeps track of retracted papers (see the related [Science magazine](https://www.sciencemag.org/news/2018/10/what-massive-database-retracted-papers-reveals-about-science-publishing-s-death-penalty) publication). 

Read the paper [Ten Simple Rules for Reproducible Computational Research](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003285) by Sandve et al.


Write a blog post addressing the questions: 

1. **Pick one of the papers Retraction Watch features on their website and describe what went wrong**. 

One paper mentioned on the Retraction Watch website is "Coronavirus disease-2019: A brief compilation of facts". The paper was retracted due to "having number of sections of content, though attributed, with high rate of verbatim similarity from another article." Basically, a significant portion of the paper was plagiarized/duplicated from a different paper and hence had to be retracted. 

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

The rule I am most likely to follow is Rule 1: For Every Result, Keep Track of How It Was Produced. I am most likely to follow this rule because it has been most beneficial to me in the past. Many times, small adjustments can be made to improve results, so it crucial to know exactly how a result is produced. It is also very important to describe how results are produced in any type of write-up of your analysis, so keep track of this throughout your project is very beneficial. The rule I find the hardest to follow is Rule 3: Archive the Exact Versions of All External Programs Used. I think this would be the hardest to follow because many times projects take a while to complete, and updates are made throughout the entire project. I don't think I would really be worried about this rule during any of my future projects because it won't have a direct impact on my results and is something that seems somewhat difficult to do. Although it would probably be beneficial, I think I would end up trying to open my project in whatever current version of a program I am using. 

{% assign num_posts = site.blog | size %}
{% if num_posts > 0 %}
## Class posts:

<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
