---
author: "Kieran Liming"
title: "Reproducibility is Still Important"
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
    
    Peng outlines that in many cases fully reproducing work in the field of biostatistics is challenging or impossible, and therefore, it is crucial that authors of work submit materials allowing for partial or complete reproducibility of their work. This often involves submitting code such as the scripts used to get to the result as well as a "target" file, which is the end results that need to be verified through reproduction.

    2. **What are Keiding's main criticisms of the proposal?**. 

    The primary criticism Keiding presents is that reproducibility from a third party is not as magnanimous or insightful as it may initially seem. In many cases, the dataset that the methods are being performed on has to be cleaned or transformed in a way that is much better understood by the researcher than by some third party. Thus, reproducibility implies some "immutable" dataset which should lead every statisitician to the same end point that the original work leads to, which cannot generally be the case due to the specific knowledge needed from the authors. 

    3. **Which point in the commentaries speaks to you the most? Why?**

   Because I understand and empathize with Peng's and Kiedling's goals, I thought the commentary brought forth by Steven Goodman was the most prominent. Keidings point that resonated the most with me was of the "immutable" dataset. A third party with little expert knowledge on the problem may have trouble reproducing the same results as the author. However, as Goodman points out, this does not preclude the author from making obscure the methods or data used to come to their results.

    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    Keidling states that he agrees with the points made by Goodman. Specifically, that better documentation can only help move the practice forward. However, he emphasizes that many of the commentaries do not engage with his main points: stronger focus on problem-driven research and the crucial relationship that substantive researchers play between the statisticians and the results.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

    In undergrad I worked with a professor and a peer on analyzing pitch characteristics from youth pitchers we had data on. Ultimately, it was very difficult to describe the changes we were making to the dataset to people not accutely aware on specifics of baseball, and thus most of the ideas we had about directions to go with the data were not well informed.
    
    We ultimately had to scrap the project due to a fundamental lack of knowledge on our end about pitch design. So if I could go back in time, it would be crucial for us to have more concrete ideas about what we were looking for before parsing through the data. As we already had "expert" knowledge on the data that was hard for us to explain to laymen. This was further compounded when we ourselves learned something new from the data that ultimately invalidated what we had worked on up to that point. 

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
