---
author: "Zirou Zhou"
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
    
    In order to get ride of fraud, the Biostatistics will requrst the paper's author to provide material, which can be used to reproduce the paper's main results. These materials need to meet some of the following standards, including the data can be access from the journal's Web site, the code are based on widly used software or the results can be reproduced within a rational numerical bound.
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    
    Keiding critic that the reserch is more than statistical analysis, especially in substantive. Keiding believe in most important research are mainly "problem-driven", which haven't found a statistical method yet. And the statisticans are resposible to make studies on these methods, while the request the reproducibility is impratical and show no respect to biostatisticans. Also reproduciblity request may produce more inbreeding as statisticians are more talking about the data set conflict rather than considering the background.
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    *The importance of independent academic statistical analysis* mentioned the necessarity about the reproducibility speaks to me the most. As currently, numbers of biostatistic work are sponcered by big medical companies. In order to get ride of data manipulation or misrepresentation, these request are necessary
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    Keiding believed the DeAngelis's main idea is still repeating the main police about the *JAMA*. And Keiding believe this is welcomed by the editors, but the *JAMA* itself is a pure auditing activity with no academic attraction, which is not important in acadimic research.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

  For now, I have being working with Fed and Berg in our department for several weeks. The main orderless things happened when we try to combined personal projects' data sets into a whole one. Even when I was using other guy's code on my local machines to reproduce the results, there's always some unexpected error messages. Currently, we are using Cybox and Overleaf to share code and data sets. Now I'm considering whether I should convince others also using Git to maintain the version control.

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
