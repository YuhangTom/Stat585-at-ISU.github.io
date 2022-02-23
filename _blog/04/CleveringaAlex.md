---
author: "Alex Cleveringa"
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
https://retractionwatch.com/2022/02/10/more-than-100-of-an-anesthesiologists-papers-retracted/  
I chose this article because I was floored by the scope of the misconduct. A single anesthesiology researcher in Japan has 117 retractions. Surprisingly,   what "went wrong" was that the researcher in question had completely fabricated or falsified the data. The lead author also presented individuals only   partially involved as co-authors, and did not get their agreement to have their names put on the papers. This isn't simply an honest mistake, but shows willful   disregard for truth and scientific integrity.
2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**  
I am most likely to follow Rule 2. I use R in all the projects I am working on for data cleaning and analysis. This makes it much easier to reproduce the same   results than if I were doing it manually in Excel, which I have done in the past. Knowing what I know now, I would not recommend doing it in Excel, even   though it may be easier for someone without experience in R. I am probably least likely to follow Rule 5. As mentioned in the beginning of the paragraph,   the results should be replicable as long as I provide the full code. It also seems easy to forget, because intermediate results are by definition not final   results. However, I do see the value in providing them to reassure people following my code that we are doing things the same way, or easier to identify   where we diverged.


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
