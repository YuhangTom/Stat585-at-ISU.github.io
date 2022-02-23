---
author: "Abraham Adokwei"
title: "Essentials of Reproducible Research"
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
  -	Paper: Primary Prevention of Cardiovascular Disease with a Mediterranean Diet. N ENGL J MED; APR 2013. 
  -	Things that possibly went wrong. 
    - Even though the authors made tremendous efforts in providing reference to supplemental materials used in various aspects of the study, there was no mention whatsoever about the Software used for data analysis, the particular version of the software and particular packages used. This according to the Ten rules by Sandve et. Al. is one contributing factor to the reproducibility of research projects. 

    - Secondly, the authors simply mentioned that Randomization was performed centrally by means of a computer-generated random-number sequence. According to Rule 6 of Sandve et al., it is important to provide vital information regarding randomization mechanisms used in a research project. 

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

- Rules easy to follow 
  -	Rule #1: Taking note of every record like parameters used in a research is an easy and essential practice to follow. This is partly because to reproduce an achieved result, one may need to use the exact parameters. 
  -	Rule #4: After being introduced to Git, I have come to appreciate the importance of using a version control for my code. This is particularly important when collaborating with other researchers or team members. 
  -	Rule # 7: Working mostly in R, I believe it is an easy thing to keep track of codes used to produce plots. 
  -	Rule #2: I have come to understand that copying and pasting a code more than once it a bad practice. A good practice however, is to write up a function for repetitive use. By this standard, I believe it is easy to avoid manual data manipulation steps.
  
- Rules that may not come easy to follow: 
  -	Rule #3: Even though archiving exact versions of programs or software used in a research has proven to help in reproducing exact results, it is easy to not thinking about this rule. I say this because I don’t remember practicing this rule in any of my previous projects. I am mostly concerned with achieving certain results that I almost always forget about the version of software I’m using. 



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
