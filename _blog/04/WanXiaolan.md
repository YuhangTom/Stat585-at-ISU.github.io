---
author: "Xiaolan Wan"
title: "Ethics and Reproducibility..."
layout: post
topic: "04"
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

## Q1 Response
The paper published in 2006, titled “Effort for Payment: A Tale of Two Markets”, was issued an expression of concern in 2021 after it partly failed a statistical stress test. 
This paper was found some issues with the reporting of the statistics. In six of the discrepancy, the outcome of the statistical test was different, which result in a “decision error”.
The mismatch between results reported as significant and the results of the recalculations, indicate that the tests are not statistically significant. These discrepancies would change the interpretation of the data that substantively alters the conclusions. 

Reference: Retraction Watch, "Prominent behavioral scientist’s paper earns an expression of concern"
http://retractionwatch.com/2021/07/29/prominent-behavioral-scientists-paper-earns-an-expression-of-concern/


2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

## Q2 Response
After I read the paper titled "Ten Simple Rules for Reproducible Computational Research", I am mostly likely to follow the rule #1: For Every Result, Keep Track of How It Was Produced. I like to write a RMD file and generate a pdf to keep track of my workflow because later on I can look into how my results were generated and check whether the code is correct. 

I found that the rule #4: Version Control All Custom Scripts, is hardest for me to follow. I usually write my code in a rmd file and click on save when I quit. I don't have the habit of tracking evolution of my code using version control system, and I am not sure how to use git to achieve this function.


 


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
