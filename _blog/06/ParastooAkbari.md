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

    1. **Summarize Roger Peng's outline for reproducibility in** *Biostatistics*. Roger Peng explains that the AER handle submissions of reproducible research after that an article has been accepted. He further explains that the submission should include data, any computer code, software, or other computer instructions that are used to compute published results. Therefore, as the last step, the AER will be able to obtain the exact results and the article is considered as a reproducible research. 
    2. **What are Keiding's main criticisms of the proposal?**. Keiding questions how Biostatistics would create a constructive approach to reproducibility. He expresses that Peng's implicit assumption is that there exists some immutable data set, directly understandable to any statistician, whose judgments about the relevant substantive context are apparently believed to be directly relevant and credible, so the substantive context has almost been ignored in Peng's outline. 
    3. **Which point in the commentaries speaks to you the most? Why?** The commentary by Cox and Donnelly speaks to me the most since they explain that publishing the full data along with the article for publication is not only for replicating the results. Then they explain with more detail and using an example from their own research about badger culling that the purpose of releasing full data can be to encourage, with discussion with subject-matter specialties, the formulation and investigation of new questions. 
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?** Keiding says that he is completely agree with their commentary and their summarization that the proposals for Biostatistics are to be welcomed even though their name and objectives are misformulated. 
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?** There was a project for one of my courses when I was an undergraduate student. For this course, we had to work with production and sales data from a factory. The main problem with making our research reproducible was that we were not allowed to release the full data, because they were considered as confidential for the factory. 


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
