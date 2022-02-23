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
I am picking the paper "study of how canvassers can sway people's opinions about gay marriage" that has been retracked from the Science magazine. The reasons why the paper got retracted were:
+ The author failed to provide the validity of the surveys conducted to conclude the results
+ There was no public data available regarding the surveys
+ Participants were given incentive to participate in the survey, so the survey does not represent the actual data.
+ One of the authors fabricated data to produce result 
+ Provide false information regarding the funding of the projects
+ And most importantly since the data was fake, it was not made public and the results were not reproducible.

2. **After reading the paper by Sandve et al. describe which rule you are most likely to follow and why, and which rule you find the hardest to follow and will likely not follow in your future projects.**
I am most like to follow the rules:
+ Archive the Exact Versions of All External Programs Used
+ For Every Result, Keep Track of How It Was Produced
+ Avoid Manual Data Manipulation Steps
+ Connect Textual Statements to Underlying Results
+ Provide Public Access to Scripts, Runs, and Results
I follow these rules because these will give me a chance to identify any error in my algorithm at an early stage. Writing scripts over using manual cleaning saves time and are more accurate. Making the data and scripts public helps someone else to reproduce the same result and also help them to run the scripts for their own project. I also describe the final result in few sentences for better understanding to the reader. 

The rules that I find difficult to follow are "Record All Intermediate Results, When Possible in Standardized Formats" and "Generate Hierarchical Analysis Output, Allowing Layers of Increasing Detail to Be Inspected". When I am dealing a project or paper deadline, I often do not write enought comments in the scripts. Also, I often skip saving the intermediate results in a standard format.

