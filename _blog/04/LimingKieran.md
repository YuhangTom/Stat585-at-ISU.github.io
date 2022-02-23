---
author: "Kieran Liming"
title: "The Issue of Ivermectin and Reproducibility"
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

Malicious changes to the data such as in the LaCour case are hard to prevent, but more rigorous checks should be built into the scientific publishing system. All too often papers have to be retracted for unintended reasons. [Retraction Watch](https://retractionwatch.com/) is a data base that keeps track of retracted papers (see the related [Science magazine](https://www.sciencemag.org/news/20 18/10/what-massive-database-retracted-papers-reveals-about-science-publishing-s-death-penalty) publication). 

Read the paper [Ten Simple Rules for Reproducible Computational Research](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003285) by Sandve et al.


Write a blog post addressing the questions: 

1. **Pick one of the papers Retraction Watch features on their website and describe what went wrong**. 

I chose to read this featured paper: https://retractionwatch.com/2022/02/11/ivermectin-papers-slapped-with-expressions-of-concern/

It is about a pair of meta-analyses purporting the efficacy of Ivermectin as an effective treatment of COVID19. Ultimately, it was found that the source of data which these analyses relied on were inaccurately reported or collected. Thus it was widely found within the scientific community and the journals for which these analyses were published that the potential decrease in mortality of COVID19 infection caused by ivermectin was spurious. However, with vaccine skepticism being a popular stance in the United States, these retractions and editors notes did little to stop popular media outlets reporting on the analyses as fact and causing Ivermectin to be a widely known "treatment" for COVID19. 

While these meta-analyses were flawed for the same reason--inaccurate data from a pivotal source--what truly failed in this case was the publishing environment for these analyses. While the US has the highest death count from COVID19 of any country in the world, more care and scrutiny should be put into publishing unverified treatments for the disease. Especially when proven efficacious treatments such as vaccinations and boosters are widely controversial in the US, it is dangerous to publish analyses that could provide fuel to the unwarranted skepticism.

3. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

The simplest rule to follow may be the last rule. Providing access to scripts, runs, and results, just requires the researcher to attach the code that they used to achieve their results. This code already exists and all it takes is making it public. Additionally, this step makes it very easy to reproduce the same results as the researcher and then to check the methodology for errors.

The hardest step in practice is likely step 2. Avoiding manual data manipulation is great for reproducibility. However, in practice it may be very challenging or burdensome to avoid. While manual data manipulation is error prone, in many cases trying to automate or avoid this step is much more cumbersome than being careful in the manual parts of your analysis.  



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
