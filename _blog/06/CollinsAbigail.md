---
author: "Abigail Collins"
title: "Blog 6"
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
        
        Roger Peng's article discusses the importance of reproducibility. In his paper, he suggests that the definition of reproducibility should be continuous and not a simple yes/no. He outlines three "pieces" of criteria that define "reproducibility", where any subset of these criteria are a benefit to biostatistics and can be deemed "reproducible". The three sub-pieces are "data", "code", and "reproducibility". Peng argues that, with the advancements of big data and powerful computing, comes a greater potential to misanalyse or make computational errors. He believes that reproducibility (or any subset of his definition) should be a minimum standard in good practice of biostatistics. 

    2. **What are Keiding's main criticisms of the proposal?**. 
    
       Keiding's main criticism of the proposal regards the importance of reproducibility itself. He argues that there is much more to statistical analysis that being able to check/reproduce correct calculations. His point was made with the idea that being able to reproduce statistical results from an statistical model, that may not have been the appropriate choice, would not have an beneficial results from reproducibility. Generally, to "check" the appropriateness of model selection or the data requires a deep understanding of the problem being examined and cannot be easily assessed. Keiding also discusses "method driven" vs "problem driven" analysis. He believes that problem driven analysis is where science makes the most advancements. However, this type of research requires close collaboration between scientists and statisticians, and again may not be easily understandable to reproduce.

    4. **Which point in the commentaries speaks to you the most? Why?**

        I align with the commentary posted by Norman E. Breslow the most. He makes a point that being able to reproduce the results of a study may create a sense of false security and draw attention away from more serious issues. Being able to reproduce computational results ignores issues such as selection bias, measurement error, uncontrolled confounding, and small sample size, which would invalidate the results of the study as a whole, so why reproduce them?
    
        
    6. **How does Keiding respond to the commentary you picked. What are his main points in his response?**

    Keiding agreed with Breslow's commentary. The commentary emphasized the key critisms Keiding had of reproducibility defined by Peng. Generally the two agrred with one another. 

    
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

    I believe the most prominent issues with ensuring reproducibility, in my experience, is ensuring that all machine dependent packages are listed within the code. I have worked in projects where I was using a previously installed package, and was unaware that it was being used and therefore did not directly load the package within my project. This led to issues with reproducibility when others tried to run the same code, and it was difficult to identify the issue. 


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
