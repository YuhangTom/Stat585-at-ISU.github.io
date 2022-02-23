---
author: "Robert Castaneda"
title: "Title of your post"
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
2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

Blog Post:
I picked a paper that wasd retracted by the Journal of Strength and Conditioning Research. One of the contributors of the paper, an exercise science graduate student admitted to faking data to use in the paper to back up his findings. A reviewer of the paper tried to reach out to the PhD student but had no luck and all the social media accounts were disabled. A third party source informed him of suspicious data. Funny thing is, a year later the same study was published by the paper without citing that it had been retracted in the first place.

I would be most likely to follow rule 10 on my future projects. I feel like that is the absolute main key for reproducibility of a project-to make your code and results public. This ensures that anyone who wanted to look over your work, or reproduce a similar result with a different project, or perhaps an extension of my project. Without doing this there is really no visible future for my project. One of the rules that I might have trouble with following on future projects is rule 2-avoid manual data manipulation steps. This really just has to do with the manner in which I code. I am trying to improve on this and instead of doing manual manipulation, create and write functions that are easily repruducible. I hope to more closely follow this rule in the future.


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
