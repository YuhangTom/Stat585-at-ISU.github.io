---
author: "Abraham Adokwei"
title: "Issues on Reproducibility"
layout: post
topic: "06"
short-topic: More on reproducibility...
due-date: 2022-03-03
root: ../../
---

## Prompt:

In 2009 one of the associate editors of Biostatistics, Roger Peng, outlined a new policy of [reproducibility](https://doi.org/10.1093/biostatistics/kxp014) for the journal. 

This triggered a response from one of the other associated editors, Niels Keiding, and subsequently a large part of volume 11, issue 3 of Biostatistics was dedicated to a discussion of issues of redproducibility. 


Read through 

- Roger Peng's [initial editorial](https://doi.org/10.1093/biostatistics/kxp014), 

- [Keiding's response](https://doi.org/10.1093/biostatistics/kxq033),

- its five [commentaries](https://academic.oup.com/biostatistics/issue/11/3),  

- Roger Peng's [response to Keiding](https://doi.org/10.1093/biostatistics/kxq032)

- and finally, Keiding's [response to the commentaries](https://doi.org/10.1093/biostatistics/kxq034)

Don't worry about the number of papers listed - these papers are all very short and easy reads. 


Write a blog post addressing the questions: 

1. **Answer each of the following questions with at least 2-3 sentences.**

    1. **Summarize Roger Peng's outline for reproducibility in** *Biostatistics*.
        - We live in a world with an increasing availability of data. Most of this data come in varying level of complexity and usually require sophisticated methods to draw insight from them. Peng emphasizes that in most situations, the possibility of inadvertent errors is on the rise. In his outline, Peng proposed three criteria for reproducing research results – Data, Code, Reproducible. To satisfy the "Reproducible" criteria, Peng recommends that authors submit all necessary materials in order to produce output similar to that obtained by the author. 
    2. **What are Keiding's main criticisms of the proposal?**. 
        -	Keiding argues that making data and code publicly available with the purpose of reproducing similar results by the authors only encourages the occurrence of poorly informed reanalyses of old data sets about which the statistician knows almost nothing about. To Keiding, there is no guarantee that the "reproduction" that comes out of this culture will benefit science.
        - Keiding further argues that Peng’s recommendations for reproducibility does not create a constructive approach to reproducibility. Thus Keiding believes that proposed framework does not provide space for imagination.  
    3. **Which point in the commentaries speaks to you the most? Why?**
        - *Analysis by D. R. Cox and Christl Donnelly*. 
        >>	The purpose of providing the full data was not primarily to encourage repetition of our own analyses, although of course anyone who wishes to do that is very welcome. Rather it is to encourage, with discussion with subject-matter specialists, the formulation and investigation of new questions, for example, about spatial–temporal aspects of wildlife ecology.
        - I am not against making data publicly available for use. This is a large extent may encourage other insightful questions that may lead to further methodological development. In my opinion, I think the objective of making data and code public for the sole purpose of reproducing similar results as a general "check" of reproducibility could be made clearer. Like they put it, this seems not merely unnecessary but a misuse of relatively scarce expertise. 
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
        -	Keiding turn to fully agree with the conclusion remarks of Cox and Donnelly. Keiding in his response emphasized the variety of purposes of making data publicly available as opposed to using the data as a check of accuracy of results. 
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

        - During one of my first collaborative project using *github*, we all had the data downloaded and so we individually had to find a way to engage the data when trying to complete a task. At this point, I believe it would've been easier to have the data added to the github repository. That way we won't each have to struggle getting hold of the data. 

Go to [https://github.com/Stat585-at-ISU/blog-2019](https://github.com/Stat585-at-ISU/blog-2019) for instructions about how to prepare and submit your blog post.


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
