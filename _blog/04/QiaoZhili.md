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

The paper [Exploring the potential effect of COVID-19 on an endangered great ape](https://www.nature.com/articles/s41598-021-00061-8) was retracted on January 25, 2022. The [retraction note](https://www.nature.com/articles/s41598-022-05893-6) states that the researchers made a mistake in the simulation studies of the potential effect of SARS-CoV-2 on a sub-population of the Virunga mountain gorilla population. They used the case fatality rates (CFRs) that was collected in the earlier period of the pandemic in China and Italy, instead of the human infection fatality rates (IFRs). The CFRs they used turn out to be heavily overestimating the death rate, thus exaggerated the possibility of extinction for the gorilla population. The article received a moderate amount of attention about mountain gorilla conservation, whereas in fact the prospect of extinction doesn’t appear to be as bad as the authors reported.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

Most likely to follow: **Rule 6: For Analyses That Include Randomness, Note Underlying Random Seeds**

This is a lesson I've learned from my own research experience. The simulation study in statistics usually contains simulation of random variables. If the random seeds are not specified, it is almost impossible to reproduce simulation results. Another issue is that, not utilizing random seeds will cause a huge problem in code debugging: If the simulation happened to be a corner case and invalidates the algorithm, there's no way we can track which specific simulation went wrong (specifically when parallel computing is utilized).

The hardest to follow: **Rule 2: Avoid Manual Data Manipulation Steps**

For specific studies, there is usually a need for manual data manipulation, feature engineering or other data-dependent stuff. Those data challenges on Kaggle are good examples. We cannot develop an universal rule of data standardization or Box-Cox transformations for all datasets.

But I do think this is a serious problem. My undergraduate major was economics, and in economics there is a notorious trick called "p-hacking". This suggests if you want some feature to be significant in a linear regression, you try different transformations on this feature until it reaches the desired p-value. This is definitely unreasonable from a statistics perspective, but it is not rare in some economic studies, and I know there are even softwares and packages that are designed to do this automatically. 


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
