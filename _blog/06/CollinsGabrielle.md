---
author: "Gabrielle Collins"
title: "Reproducible Research guidlines"
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
    In order for an article to be considered reproducible, 3 different criteria need to be met. A subset of these criteria can also be met, for example, if data cannot be publicly available.  The three criteria are: 1. Data is made available 2. Any software/code used to compute results is made available 3. An article is deemed reproducible if the AER succeeds in running the code and gets the same results as the initial author. Currently, only submissions using R are being accepted. 

    2. **What are Keiding's main criticisms of the proposal?**. 
    Keiding's biggest criticism is that Peng's outline for reproducibility largely ignores the fact that there is much more involved in statistical analyses than the correctness of calculations. There is a long process and discussion between the scientists and statisticians of a given project to even get to the data set that is used in said calculations, and that process cannot be summarized in a R file. He also discusses how making a data set available with little background information on the subject encourages the issue of staticticians blindly working with data, without fully understanding the context of the problem. 

    3. **Which point in the commentaries speaks to you the most? Why?**
    I think Cox and Donnelly's comment spoke to me the most. I agree that reproducibilty is important and well-intended, however Peng's emphasis on reproducing the exact study for merely verification of results seems to be slightly misguided in my opinion. I agree with Cox, that the intent of having reproducible projects should be to spark new ideas and questions for subject-matter specialists within that field. I think this is how new research ideas and projects could be started. 

    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    He fully agrees with the conclusion made by Cox and Donnelly, that making data available serves a variety of services.  
    
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

Since the majority of my projects have been in the classroom setting, I don't think making datasets available would really be an issue in terms of reproducibilty. However, I do tend to only focus on whether my code will run locally on my own machine, so I think making the code available in a way that is reproducible would be the most prominent issue. If I could go back in time, I would try to write code in such a way that makes it easy to reproduce and easy to follow. I could do this by fully defining functions used and created and by keeping track of the versions of packages I used. 


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
