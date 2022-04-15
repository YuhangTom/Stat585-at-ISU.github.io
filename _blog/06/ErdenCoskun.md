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
    
According to Peng, there are various reasons for the need to publish repeatable research. One factor is that researchers are increasingly looking into weak connections and complex interactions. Investigators' use of complex high-dimensional databases and processing capacity increases the risk of detecting misleading connections. The publication of fraudulent research in the biomedical literature is a second cause. Peng proposes "reproducible research," which involves making data sets and computer code available to others for the purpose of checking published results and conducting alternative analyses. In addition, the Associate Editor for Reproducibility (AER) specifies that while evaluating the reproducibility of an article, it will evaluate three separate factors. 1. Data: The analytic data used to obtain the main findings is made available on the journal's website. 2. Code: Provide any computer code, software, or other computer instructions required to compute published results. 3. Reproducible: An article is considered reproducible if the AER is able to run the code on the data provided and produce results that are consistent with the authors' claims. However, authors can choose to meet only a portion of these requirements.  
    
    
    2. **What are Keiding's main criticisms of the proposal?**. 
Keidings claimss that reanalyses of old data sets removed from their original context run the risk of distancing methodological advances from the problems they were supposed to assist solve. Instead, he highlights the importance of putting a greater emphasis on problem-driven research. He also says that reanalyzing data from repositories will not lead to "high-quality applied statistical work," which he describes as close contact between the statistician and the substantive researcher.
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
I agree with Goodman's assertion that if scientists are aware that their studies may be examined by others, they will improve the quality of their work before submitting it for publication. The point made by Goodman is the one that resonates with me the most because in my opinion education research findings should be based on high-quality analyses as they can have a significant impact on policy and practice development, which can have a great effect on students' academic lives and careers in the future.

    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
Keiding agrees with Goodman's point. He acknowledges that improved documenting of computations will improve the statistical refereeing quality in subject-matter publications.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

In Stat 520, I collaborated with a group of friends on the final assignment. To conduct the required analysis, each team member created his or her own codes. When we got conflicting results, we looked at the independently produced programs and figured out what was causing the discrepancies, and we were able to quickly come to a consensus.  There was no data related component of the difficulties because data was provided by the instructors in these assignments. However, for my dissertation, I am currently working with High School Longitudinal Data (HSLS:09). It's a large scale dataset, so I can see how different researchers can come up with different answers to the same research issue depending on how they handle the data. Changes in how missing data is handled, outliers are classified, and how participants in different groups are characterized can all lead to different conclusions for the same underlying research questions. Based on my own experience, I believe that supplying the data and descriptions used in data processing, as well as the research codes, are two major characteristics of reproducible research.


 



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
