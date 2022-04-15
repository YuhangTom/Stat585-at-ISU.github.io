---
author: "Yunhui Qi"
title: "More on reproducibility by Yunhui Qi"
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
    
   There are three dimensions of reproducibility: data should be available, code should be available, and can be executing to generate the results. He proposed to submit the main script including code for all analysis, target file including the results, and other files need to executing the main to generate the target.
   
  
    2. **What are Keiding's main criticisms of the proposal?**. 
    
     I think his main point is that the reproducibility implementation proposed by Peng put too much importance on the technical tools for the numbers and the code, but ignoring the substantive context.
   
   Although this is not relevant, I felt angry about the criticisms. In keiding's opinion, our statisticians are the ones who only know coding on data, do not care about any background. He even thought the requirement of  Journal of the American Medical Association is a kind of mistrust of his colleagues. My point is reproducibility is the basic requirement for any publication no matter in what area. If you cannot reproduce your results, the results are not reliable.
   
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    Steven N. Goodman's commentary. He pointed out the at least we should make some efforts. I understand reproducibility for the papers in biology is not that easy as in statistical papers. But at least we should admit that reproducibility should be cared about. Any efforts aiming at achieve reproducibility will contribute to the transparency, complete, validation of research.
    
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    He said "he was persuaded by Goodman's point that better documentation of the computations will enhance the quality of statistical refereeing in subject-matter journals."
    
    His main point in his reponse is that reproducility of statistical analysis of papers in biology is not a big point, it does not benifit the development of science, it should not be a rule to waste the time of scientist.
    
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

To be honest, I did not feel much difficulty in ensuring reproducibility on the data related aspects. Some may be in simulation, I usually set random seeds to ensure the reproducibility.  I believe reproducibility is the basic rule for any research. 


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
