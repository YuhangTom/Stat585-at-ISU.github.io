---
author: "Wangqian Ju"
title: "Retraction and rules for reproducibility"
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

The article I read was [this one](https://retractionwatch.com/2022/02/14/journal-retracts-a-paper-then-publishes-in-an-issue-11-months-later/#more-124232), which talks about a retracted paper being published in an issue without the retraction notice. The publisher should handle the record of a retraction more carefully since they are responsible for their contents and the readers should be aware of the story behind the retraction record.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

I'm most likely to follow the first rule: "for every result, keep track of how it was produced". This will make sure the reproducibility of my results. And one thing that I unconsciously ignored before is the version of the packages involved in the project. The version change of a package should not but could lead to unexpected result change, which destroies the reproducibility of the result. 

I think the rule that is hardest to follow is rule 9: "connect textual statements to underlying results". Although Sandve makes sense in the explanation of the section, it's hard for me to imagine actually following this rule. 

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
