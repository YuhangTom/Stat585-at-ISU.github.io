---
author: "Lin Quan"
title: "Reproducibility"
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
    
    Roger Peng pointes out that the biostatistics paper should meet a three-dimension standard of reproducibility. The author should ensure that the analytic data is accessible. The code that were used to coumputed published results should be provided. The article is reproducible if the AER could excute the code on the data provided and produce the results matching those that authors claim within reasonable bounds. 
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    
    Keiding's main point is that Peng’s editorial encourages others to conduct the alternative analyses which concerns the substantive issues, but the term “reproducible” is a misnomer. There is much more to the statistical analysis than the correctness of calculations. We should avoid encouraging poorly informed reanalyses of old data sets about which the statistician knows almost nothing. He think there is no guarantee that the “reproduction” that comes out of this culture will benefit science.
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    I think one point from D. R. Cox speaks to me most. He thinks the purpose of providing the full data was not primarily to encourage repetition of our own analyses. Rather it is to encourage, with discussion with subject-matter specialists, the formulation and investigation of new questions. I think this is main purpose for the authors to provide the data. We can use the same data for analysis and we can find similarities and differences with the authors' results.

    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    Keiding fully agree with his conclusion. He thinks that Cox acknowledges the variety of purposes of making data available, exemplified with his own work. He has two main points. First, We should focus on problem-driven research in biostatistics. Reanalyses of old data sets detached from their original context run a risk of alienating the methodological developments from the problems they were intended to help solve. Second, High-quality applied statistical work requires close contact between the statistician and the substantive researchers. But we cannot assure it.

2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

For my research project, I need to update my results weekly. But sometimes, it's hard for me to reproduce the results or graphs that were generated months ago. If I go back in time, I will have the detailed annotations for each step and code. Every week, I need to make a documentation to record the updated steps and code.

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
