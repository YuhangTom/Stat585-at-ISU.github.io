---
author: "Xiaolan Wan"
title: "Roger Peng"
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
        Roger Peng's paper emphasizes the necessity to build a standard of reproducibility to avoid the potential fraud and inadvertant errors. He considered three different dimensions of reproducibility, including Data, Code, and Reproducible, at least one of which should be met. Peng also gave instructions on submission process and listed necessary materials to submit with the aim to satisfy the “reproducible” criterion.


    2. **What are Keiding's main criticisms of the proposal?**. 
        Keidling's main criticism is that there is much more research and statistical analysis than the correctness of calculations. He emphasized that we should focus on “problem-driven” research, which make more real progress. Some mandatory reproducibility requirements in the journal ridiculed authors' profession to check other's reproducibility, and it is impractical to devise a reanalysis template that can capture this whole process. 


    3. **Which point in the commentaries speaks to you the most? Why?**
        I echo with the point put forward by Norman E. Breslow. He argues that being able to reproduce the results would provide  a sense of false security, which divert the attention away from the more serous problems. The focus of reproducibility ignores issues including selection bias, measurement error, uncontrolled confounding, and small sample size, which would invalidate so much of the results of epidemiologic research. The primary benefit would come from alternative analyses, instead of reproduction of the published results.

    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
       Generally, Keiding was in the line with Breslow's viewpoint. He emphasized the importance of reproducibility as well as the key critisms proposed by Donoho and Goodman.
    
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**
    I have been doing a survey project with my advisor since the last year. He sent me the survey data that have already well cleaned by himself, and asked me to do another part of data analysis. However, I found there were many variables and numbers without any definitions or explanations. It is very hard for me to understand the meaning and how some variables were generated. If I could go back in that time, I would suggest my advisor to write an encoding book at first, to give clear definitions and explainations for these variables. 
    


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
