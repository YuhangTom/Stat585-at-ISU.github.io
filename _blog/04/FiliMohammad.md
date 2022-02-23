---
author: "Mohammad Fili"
title: "Blog #4"
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

<span style="color: purple">
I selected an [article](https://retractionwatch.com/2021/07/30/a-very-unfortunate-event-paper-on-covid-19-vaccine-hesitancy-retracted/#more-122763) which explained a case that a paper was retracted because the authors didn't have the license to do text mining on a data base.
In the article, it was mentioned that a group of researchers from the University of Ottawa, published a paper on tracking Covid-19 hesitancy, but later on, they found problems regarding the data use permissions. They assumed that since they have access to the contents through the library, they are also allowed to mine it as well. Finally the authors agreed to retract the paper.
</span>




2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

<span style="color: purple">
_One rule that I am most likely to follow is_: <br>
storing raw data for each plot. It happened a few cases for me that, I generated a plot, but later on I needed to reformat it, or even change it. But since I didn't have a copy of the raw data, I had to redo the analysis to generate the data first.<br> <br>
_One rule that I think is challenging is rule 8 (Generate Hierarchical Analysis Output)_: <br>
Sometimes the analysis contains various stages, and apply this rule may be time-consuming. Moreover, not all outputs are necessary to keep. They might not be relevant, may be used for one time only, or might be generated very easily if needed.
</span>







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
