---
author: "Alex Cleveringa"
title: "Blog 6: Bolg 6"
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
The standards of reproducibility for *Biostatistics* include three dimensions:  
data, code, and results. The data must be provided, the code used for analysis  
must also be provided, and the Associate Editor for reproducibility must be able  
to execute the code on the data that produces the same results as the original  
authors.
    2. **What are Keiding's main criticisms of the proposal?**. 
Keiding's main criticisms are that he thinks Peng trivializes the work that they do by focusing on loading in the data and the code, hitting "Run", and getting the same results out. Keiding states that "There is usually much more to "research" than the statistical analysis, and there is much more to the statistical analysis than the correctness of calculations." By encouraging the reuse of old data sets about which other statisticians know very little, poorly informed decisions will be made. 
    3. **Which point in the commentaries speaks to you the most? Why?**
I found the commentary by Donoho (https://academic.oup.com/biostatistics/article/11/3/385/257703)
to be the most interesting. The reality that we often forget what was done with  
our own data is something I have experienced with programs that don't use code.  
I have also currently experiencing the frustration and confusion with trying to 
replicate results reported by others who don't have clear documentation for how 
they obtained their results. I recognize how much time it can save all parties  
involved. I am also intrigued by the quote "The actual scholarship is the full  
software environment, code, and data, that produced the result." It's a  
perspective shift that focuses on the entire process, not just the end.
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
Keiding's main points in his response to Donoho is that improving the data  
documentation is long overdue, and that Donoho does not explain what better  
documentation will look in practice with interdisciplinary collaborators.    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**
One problem I am currently experiencing is that I have a data set that was  
collected by another organization, which was collected over 13 years by many  
different groups. I found some concerning values in the data (impossibly high organic matter values in soil). I have been trying to understand the process by  
which their values were obtained so I can recreate it to see how it happened. We  
created our own procedure of retrieving the same information and compared it to  
their results, and it does not match. This could be caused by a number of  
reasons, and as far as I can tell there is no way of being able to confirm which  
one is the culprit.

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
