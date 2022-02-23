---
author: "Abigail Collins"
title: "Publication Retraction Thoughts"
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

1.) I read an article titled "University Recommends Seven More Retractions For Psychology Researcher" posted by Retraction Watch (https://retractionwatch.com/2022/01/31/university-recommends-seven-more-retractions-for-psychology-researcher/#more-124090). This article discusses how a psychology researcher from The Netherlands was found guilty of misconduct due to data and experiment manipulation, as well as fabrication in grant proposals. Lorenza Colzato was first found guilty in 2019, however an investigation conducted by Leiden University in November 20021 revealed that an additional 15 publications by Colzato contained misconduct. Colzato changed the design of her experiment after data/results were concluded by adding an additional control group to the dataset. She also omitted some of the data to alter results, therefore invalidating her study.


2.)	I believe rule number 1 is the most important rule listed, and the rule that I tend to follow most frequently. This rule reflects the importance of “analysis workflow”, which, in summary, is keeping track of every step of the analysis in a detailed, structured, way. This allows for reproducibility by you, and peers, which allows for validity checks, and quick changes if need be. Personally, doing this throughout my own research has proved to be very helpful. When working with large data over an extended period of time, it has been useful to go back to early steps to track progress and understanding. The organization and detailed structure of tracking analysis has made sharing code with others much easier as well. 

Rule 10 is the rule that I tend to adhere to least often. Although I understand the importance of making your work easily and publicly accessible to allow for peer review, often it is difficult due to confidentiality restrictions on datasets, ect. In the corporate world, both data and code produced by employees is not allowed to be shared. However, I do think sharing your ideas of analysis and code in an academic setting should be done because it allows you to learn from others (which is a great way to learn). Although I tend to share code/ideas with my fellow classmates, I have not had to publicly share anything due to the casual structure of the analysis (ie no publications).





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
