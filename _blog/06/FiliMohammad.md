---
author: "Mohammad Fili"
title: "Reprodicibility Issues"
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
    
    He described different aspects of a reproducible study. By providing the code and data, journals can run the same analysis with the environment needed to run those codes, and if the same results are obtained, then it is confirmed as a reproducible study. In fact he thinks that making this check before publication is a beneficial and required step.
    
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    One of the things that he mentioned was the fact that the reproducibility may not be only about the correctness of calculations, but may need insight regarding the context and the appropriateness of the data used in that study. In that case, there should be sufficient info on the subject so that the reserachers of other fields clearly understand the problem. 
    He also mentioned that the journal editors should be more concerned about the problem-driven methods than method-driven studies since the latter can set apart methodologies from their applications (that were specifically intended to solve).
    
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    Cox's point of view was interesting to me. He mentioned that sometimes datasets are became available not for the purpose of regenarating the solutions or double-checking the procedure but to encourage others investigate other formulations and new aspects of the problem.
    He also mentions that replicating the analysis before publishing a paper, is not only necessary but also misuse of the expertise that could be applied in a more productive manner.
    
    
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    Keiding acknolwedged cox's point of view and mentioned that this is true that making a dataset available can have other purposes than just replicating the analysis.
    Unlike Peng, he belives that the number of experts considered as leaders in this field may not be that many, so there exist a lot of authors who are not aware of the substantive details of the problems they are working on. This is a matter that he thinks editors has focused on not as much as needed.
    
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

I was working on a machine learning project and at some point we wanted to apply an unsupervised learning technique on data, but due to the random nature of the problem, we realized that the set of results obtained was different than the one generated earlier. This kinds of discrepancies can affect the analysis significantly. 
so I would try to make it reproducible by setting a random seed for the problem. This ensures that the the same set of results will be obtained throughout different runs of the algorithm.



Benefits of reproducibility: 

1. It prevents research misconducts.
2. It helps others trust the developed method in a study by getting the same output, so that others can build upon the previous studies with confidence.


Issues: 
1. Sometimes make the data available may not be possible for authors.
2. It should be noted that making a dataset available may have a different purpose than just double-checking, so we can work on other aspects rather than just rerunning the same analysis.





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
