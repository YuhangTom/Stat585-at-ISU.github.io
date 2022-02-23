---
author: "Bufei Guo"
title: "Blog 4"
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

The article "Tumor necrosis factor overdomes immune evasion in p53-mutant medulloblastoma" is retracted owing to issues with the integrity of the data presented.
There are inconsistencies in the flow cytometry, which is the machine used to collect many of the key data in the paper. The photomultiplier tube voltages should
have been kept the same throughout an experiment to make the samples comparable. However the voltages has been selectively altered from some of the samples. The
senior author of the paper has been tried to replicate the major experiments in the paper but none of them are able to replicate many of the key findings. Based on
these results, they decided that they could no longer stand by the conclusions of the paper, and that it would be appropriate to retract it.

3. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

The rule I found most useful and most likely to follow is *Rule 1: For Every Result, Keep Track of How It Was Produced*. In my point of view, this rule
includes but limited to giving comments when writting code, keep "README" files for materials/data used and make previous results well organized.
Following this rule will help to guarantee the credibility, stability and reproductivity of results. Aslo bookkeeping how every results are produced 
make error checking easier when something went wrong.

The rule I find hardest to follow and will likely not to follow is *Rule 6: For Analyses That Include Randomness, Note Underlying Random Seeds*. Although I will
set a random seed when I do simulation, but somehow I found that the same random seed will generate different simulation results across different computers, 
if they do not have the same version of R. So when I switch between my desktop and laptop, whose R version are different, I already break this rule. In
statstics, out conclusion/results shoule be random seed independent, which means achieving approximately equal results when change seed is acceptable.

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
