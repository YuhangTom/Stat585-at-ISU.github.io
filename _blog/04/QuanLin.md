---
author: "Lin Quan"
title: "Ethics and Reproducibility"
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
The investigation resulting in the retraction was triggered by two Berkeley grad students who attempted to replicate the study and discovered that the data must have been faked.
 
[FiveThirtyEight](https://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/) has published an article with more details on the two Berkeley students' work.

Malicious changes to the data such as in the LaCour case are hard to prevent, but more rigorous checks should be built into the scientific publishing system. All too often papers have to be retracted for unintended reasons. [Retraction Watch](https://retractionwatch.com/) is a data base that keeps track of retracted papers (see the related [Science magazine](https://www.sciencemag.org/news/2018/10/what-massive-database-retracted-papers-reveals-about-science-publishing-s-death-penalty) publication). 

Read the paper [Ten Simple Rules for Reproducible Computational Research](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003285) by Sandve et al.


Write a blog post addressing the questions: 

1. **Pick one of the papers Retraction Watch features on their website and describe what went wrong**. 

The papers Retraction Watch feature I choose is "Journal retracts a paper, then publishes it in an issue 11 months later". <i>The Journal of Strength and Conditioning Research </i>(JSCR) was retracted two papers because a graduate student had committed misconduct in the work. As Universidad Autónoma de Madrid professor Carlos Balsalobre noticed that the paper was retracted due to data fabrication, which covers the validity of a technology that is no longer in the market.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

I'd like to follow rule 1 and rule 7. For rule 1, it's important to keep track of how every result was produced. For every involved step, we should make sure that every detail that may influence the execution of the step is recorded. If we get some error or wrong result, we can easily check the details. For rule 7, It's essential to store raw data behind plots. Not only is it benefit for us to modify figures, but also it is easy for others to generate the same figures from raw data. For example, we use R programming to plot figures. If we store the raw data, others can easily plot the same picture using other programming (such as Python). I think it's hard for me to follow rule 3 in my future projects. I always update the version when they have the latest one. And I do not record the version of the package or software when I use it. If I update the version of a packages or software, I will rerun the script to ensure it works.

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
