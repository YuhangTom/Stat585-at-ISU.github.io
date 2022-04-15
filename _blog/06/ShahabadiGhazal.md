---
author: "Firstname Lastname"
title: "Title of your post"
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
    He considers three different dimensions for reproducibility in Biostatistics. First, the origins of data should be mentioned. Second, the applied code should be provided.       And the last, the results of the provided code with the provided data should be matched with the author's results.    
    3. **What are Keiding's main criticisms of the proposal?**. 
    The main criticism is that research is not just statistical analysis and statistical analysis is not just about the correctness of the calculations. We should pay attention     to other aspects of research.
    5. **Which point in the commentaries speaks to you the most? Why?**
    The point is that sharing some information causes authors to improve their work before sharing any data. This can prevent from happening something bad in the medical world.
    The first reason that I agree with this point is that authors do not like sharing any wrong information, which endangers their credit. Besides, if some information is           available, the following works can be done very quickly and accurately. 
    7. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    I am persuaded by Goodman's point that better documentation of the computations will enhance the quality of statistical refereeing in subject-matter journals.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**
I remember I did a project for my MS thesis and produced some data to test my code and save the result. Unfortunately, I did not save any information about the test problems that I produced randomly. When I submitted my paper, the reviewers gave me some comments which I needed my test problems to revise my paper. If I could go back, I would save all of my tests and results and any middle code I wrote.


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
