---
author: "Yuhang Lin"
title: "Retraction Watch and Rules for Reproducible Research"
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

    The editor pointed out that on the
    [Top 10 most highly cited retracted papers](https://retractionwatch.com/the-retraction-watch-leaderboard/top-10-most-highly-cited-retracted-papers/),
    the second most cited paper
    [Ileal-lymphoid-nodular hyperplasia, non-specific colitis, and pervasive developmental disorder in children](https://www.thelancet.com/pdfs/journals/lancet/PIIS0140-6736(97)11096-0.pdf)
    has even more citations after retraction.
    That's interesting,
    and I checked the
    [database](http://retractiondatabase.org/RetractionSearch.aspx#?ttl%3dIleal-lymphoid-nodular%2bhyperplasia%252c%2bnon-specific%2bcolitis%252c%2band%2bpervasive%2bdevelopmental%2bdisorder%2bin%2bchildren)
    to see why it is retracted.
    There are quite a lot of reasons for this retraction compared with others.
    
     1. Falsification/Fabrication of Data
     1. Investigation by Company/Institution
     1. Investigation by Third Party
     1. Lack of Approval from Company/Institution
     1. Lack of IRB/IACUC Approval
     1. Manipulation of Results
     1. Upgrade/Update of Prior Notice
    
    Among all these reasons,
    the one that is the easiest for me to understand but the most intolerant is "Manipulation of Results".
    That is obviously a violation of the basic ethics of conducting research, drawing conclusions, and guiding the public.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**

    I am already adapted to rule 1, rule 6, and rule 7 in my research procedure,
    mostly because I have experienced "with the wisdom of hindsight, contemplate the missed opportunity to ensure reproducibility" as described in the paper,
    and in the future, I would pay more attention to format the output,
    either final or intermediate.
    
    Rule 3, 4, 5, 8, and 10 mentions something that I ignored, at least before reading through the checklist questions provided in the first-week lecture and this paper.
    Among them,
    rule 3,
    which is storing the exact versions of all external programs used seems to be the most difficult one for me,
    especially for storing a full virtual machine image of the operating system and program.
    It seems to be very inconvenient and unrealistic,
    as the program may have updated a lot throughout a project,
    and it is hard to save every virtual image of them.
    
    As for rule 2,
    I never thought of modifying the data set manually before,
    and I am 100% sure I wouldn't do that in the future either.



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
