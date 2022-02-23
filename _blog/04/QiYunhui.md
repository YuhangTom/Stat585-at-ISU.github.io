---
author: "Yunhui Qi"
title: "Ethics and Reproducibility"
layout: post
topic: "04"
short-topic: "Ethics and Reproducibility..."
due-date: 2022-02-17
root: ../../
output: github_document
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

I picked:

Authors retract, resubmit “very poorly conducted” meta-analysis of COVID-19 treatment

(https://retractionwatch.com/2021/12/02/authors-retract-resubmit-very-poorly-conducted-meta-analysis-of-covid-19-treatment/)

The retracted paper is called “A meta-analysis of granulocyte-macrophage colony-stimulating factor (GM-CSF) antibody treatment for COVID-19 patients”

In their meta analysis, they include 12 analysis to review, and the authors claim the potential benefit of GM-CSF antibody treatment for COVID-19 patients after the analysis. However, among the 12 analysis, there are only 2 analysis studying anti-GM-CSF-therapy and none of them are statistically significant, the other 10 analysis evaluated IL-6 inhibitors compared to control groups. The potential benefit to COVID-19 patients may come from the IL-6 inhibitors instead of the GS-CSF antibody treatment. The conclusion that GM-CSF antibody treatment is arrived base on the wrong analysis, thus is wrong. 

These problems are pointed out in a letter to the Editor https://journals.sagepub.com/doi/full/10.1177/20406223211050495



2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

The rule I am most likely to follow is Rule 4: Version Control All Custom Scripts. I have never done this before, all the scripts are stored in my computer and cloud. The problem is that in for some code script, I need to try lots of models, different tuning parameters, e.g the tuning parameters in neural network. But every time I open my script, it is really difficult to read the code script again (too long) and find what I changed last time. I believe the version control can make it clear.

The hardest rule is Rule 3: Archive the Exact Versions of All External Programs Used. Because R packages are updated frequently, and so do python packages. And there are history version of packages online. From the papers I have read, it is enough to just store the version indices of the packages used and provide them in our own paper.





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
