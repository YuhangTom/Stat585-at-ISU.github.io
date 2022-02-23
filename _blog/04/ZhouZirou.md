---
author: "Zirou Zhou"
title: "Blog 04"
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

*Paper blaming COVID-19 on 5G technology*(https://retractionwatch.com/2020/07/26/paper-blaming-covid-19-on-5g-technology-withdrawn/) was withdrawed before nominated as one of the worst papar candiate in 2020. The author has no idea of 5G technology and in the paper he mentioned the 5G can cause 720! kinds of diseases. However, the fact is there're 13,000 diseases in the ICD-10, 720! is way more greater than this number. These evidences show the author lack of basic science trainning.

And the Retraction Watch believe, even it is published by Biolife, this is a paper slip through the net. The reasons are first, this paper has no responded to a request for comment and second, there're too many publication online during the pandamic and claimed they are peer reviewed.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

*Always Store Raw Data behind Plots* is the most likely to follow. First of all, for most of time, I will use R to draw plots, which means I can easily use *write.csv* function to save the data in a csv form and keep it in the working directory. And also, for small database I can use *table* in LaTex direclty and for a big data I can save it on server for others to download. 

*Avoid Manual Data Manipulation Steps* is the most likely not to follow. As most of the times, in simulations, the parameters' setting are purposed in achieve some specific results, which means, in process, I will need to change different parameters' pairs. What I can do is record the parameters' setting and results, but all request manually working.

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
