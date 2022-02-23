---
author: "Firstname Lastname"
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

I examined "Clinical and Scientific Rationale for the “MATH+” Hospital Treatment Protocol for COVID-19" article from Journal of Intensive Care Medicine. The authors reported the mortality rate among 191 patients who received a therapy of methylprednisolone, ascorbic acid, thiamine, heparin and co-interventions (MATH+)
as 6.1%, as compared to mortality rates reported in the literature ranging from 15.6% to 32%. The authors stated that these data “provide supportive clinical evidence for the physiologic rationale and efficacy of the MATH+ treatment protocol.” However, the article was retracted after the journal received a notice from the hospital where these patients received MATH+ therapy indicating that the mortality rate was 10.5%, rather than 6.1%. In addition, of those 191 patients, only 73 patients (38.2%) received at least 1 of the 4 MATH+ therapies, and their mortality rate was 24.7%. Only 25 of 191 patients (13.1%) received all 4 MATH+ therapies, and their mortality rate was 28%. Because of inaccurate report of COVID-19 hospital mortality and concerns that are material to the article’s findings, the article was retracted.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

Although all of the ten rules Sande et al. mentioned are very important and should be followed, I will most likely follow is rule two: avoid manual data manipulation steps. I easily lose track of manual manipulations I make if I do not take notes about them. Instead of taking notes somewhere else about the changes I make in the data, it makes more sense to rely on the execution of programs to modify data. Modifications are kept in the code automatically. I find rule eight, generating hierarchical analysis output that allows layers of increasing detail to be inspected, the hardest to follow. Although I find the idea of keeping the full data underlying each summarized value and generate, inspect, and validate the detailed values underlying the summaries at least once beneficial, I doubt that I can develop such a habit.  

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
