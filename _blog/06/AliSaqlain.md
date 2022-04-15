---
author: "Saqlain Ali"
title: "Reproducibility in Biostatistics"
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
        There are three different criteria when evaluating the reproducibility of an article namely, data, code and reproducible. The data from which the analytical         results were derived must be made available to the journal's website. Code written on computer or any software used must be provided with detailed                   information and lastly, the article will be considered as reproducible if it succeeds in executing the code on the data provided and produces results               matching those that the authors claim are reproducible.
        
    2. **What are Keiding's main criticisms of the proposal?**. 
        Keiding's main criticisms of the proposal are the following:
        1. There has to be sufficient information for another interdisciplinary group of researchers to understand the substantive context and the strengths and                weaknesses of the data.
        2. For the quest of reproducibility, it may lead us further into conclusions of data sets only but then the real context will be long forgotten.
        
    3. **Which point in the commentaries speaks to you the most? Why?**
        To make important sets of data available for independent study by Dr. Cox and Dr. Donnelly.
        The purpose of providing the full data was not only to encourage repetition of our own analyses but also for discussion with subject-matter specialists, the         formulation and investigation of new questions, for example, about spatial–temporal aspects of wildlife ecology as stated by Dr. Cox and Dr. Donnelly.
        
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
        Dr. Cox and Dr. Donnelly acknowledge the variety of purposes of making data available, exemplified with their own work on badger culling. Dr. Keiding fully         agree with their conclusion.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

    I have worked on a project for predicting flight prices. The most prominent issues with ensuring reproducibility results was to make the dataset public. Another     one was to make a note which libraries were used and their respective versions and save it in a text file, so that anyone can reproduce the same analysis as         mine.
    If I could go back in time then I would have given the strengths and weaknesses of the data such as the data that I have worked with only contains the               information about Indian Airlines of the year 2019 and not all of the Indian airports are present in the dataset.


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
