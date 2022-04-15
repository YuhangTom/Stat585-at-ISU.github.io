---
author: "Bufei Guo"
title: "Blog 6: More on reproducibility"
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
    Roger's *Reproducible research and Biostatstics* has three parts. In the first part, Peng states the necessity of publishing reproducible research-- make
    associative researches easier and prevent fradulence. The second part includes criteria of evaluating reproducibility: Data, Code and Reproducible. The last 
    parts are instuctions for authors, like materials/file/softwarse needed to satisfy each criteria of reproducibility together with an example demonstrating
    those instructions.
    2. **What are Keiding's main criticisms of the proposal?**. 
    Keiding thinks that it is more important to forcus on the statistical analysis than the correctness of calculations.Poorly informed reanalyses of old data
    sets should not be encouraged. 
    Keiding argues that exact recovery of result is unrealistic, as the results are often minor part of statistical analysis and exsitence of rounding error.
    Also, releasing of data sets is not allowed in many situations. Even when the data is made avilable, such "immutable" data set under Peng's assumption
    does not exist.
    3. **Which point in the commentaries speaks to you the most? Why?**
    In "An invitation to reproducible computational research" by David Donoho, the author states that *Computational reproducibility is the means by which the
    published "knowledge'' becomes really available to a widespread audience*. Focusing on computation reproducibility won't whittle away the importance of
    statistical analysis. In some sense, release of computational details, i.e. code and algorithms, will help people to better understand the underlying
    methodology. Abnormal results in the process of trying to reproduce the results is not necessarily a bad sign, it could help people locate potential
    problems and further improve their statistical models.
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    Keiding states that Donoho's attempt to improve the level of documentation during the whole research process and all the way to the publications is
    commendable but overdue. *Donoho does not explicitly mention how these policies should interface with the substantive context and the interdisciplinary
    collaborative groups that are usually necessary to generate scientific results of importance*, said by Keiding. In Keiding's response, Donoho's points
    are good but not realistic as Donoho does not suggest how those suggestions can be executed in substantive context and interdisciplinary collaborative
    groups. Although I think Donoho's commentary already made his point, in Keiding's view it does not argue with his main points: need a stronger focus on
    problem and reanalyzing data does not assure high-quality work.
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**
The most prominent issues with ensuring reproducibility of research results is to make sure each part understand the data structure and make sure the data is
clean, i.e. how the data is collected and what each covariates represents. Because different interpretation of the data might lead to different results. For 
example, when we are presented with a field layout of the crops, is there any replication, if yes how each genotype distributed within each blocks and how each
blocks are replicated within each big replication. It might be difficult to understand the field layout directly from the .csv file and misinterpretation will make
previous model useless. Also, real data sometimes have errors, like duplication, missing or the same object having different names. Sometimes uncleaned data might
lead to different results. I might be able to clean the data more efficiently if I go back in time with more knowledge in how `R` works with data. And learn to ask
my partners questions that will make my undertanding of the data better.

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
