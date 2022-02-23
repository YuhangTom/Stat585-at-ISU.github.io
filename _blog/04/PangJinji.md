---
author: "Jinji Pang"
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
The investigation resulting in the retraction was triggered by two  Berkeley grad students who attempted to replicate the study and discovered that the data must have been faked.
 
[FiveThirtyEight](https://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/) has published an article with more details on the two Berkeley students' work.

Malicious changes to the data such as in the LaCour case are hard to prevent, but more rigorous checks should be built into the scientific publishing system. All too often papers have to be retracted for unintended reasons. [Retraction Watch](https://retractionwatch.com/) is a data base that keeps track of retracted papers (see the related [Science magazine](https://www.sciencemag.org/news/2018/10/what-massive-database-retracted-papers-reveals-about-science-publishing-s-death-penalty) publication). 

Read the paper [Ten Simple Rules for Reproducible Computational Research](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003285) by Sandve et al.


Write a blog post addressing the questions: 

1. **Pick one of the papers Retraction Watch features on their website and describe what went wrong**. 

- The paper I picked is "Analysis of Ten Microsecond simulation data of SARS-CoV-2 dimeric main protease ".

- The reason for the retraction is :
The authors have withdrawn this manuscript because of a violation of research ethics. Unknown to the first author, the corresponding author - the main designer of the project - did not obtain consent for the use of a data-set. Therefore, the authors do not wish this work to be cited as reference for the project.



2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

- I feel Rule 7 is most likely to follow as I already done so. Exactly like the paper mentioned, I usually modify my figures multiple times before getting a final edition. Thanks for R markdown, I can make modification easily using the same data set and save the work along with textual explanations. 

- I feel Rule 8 is the hardest to follow. For sure this rule is also very essential, but it's very hard for me to achieve that goal. Maybe that's because my main research is about microbiology, the data will be showed on paper is usually highly summarized.Some essential intermediate data might be included as supplement, but usually we do not show intermediate results.




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
