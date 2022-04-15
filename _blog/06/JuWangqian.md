---
author: "Wangqian Ju"
title: "Thoughts and discussion on reproducibility"
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
    
    -   Data: are made available online and are ensured to have all necessary permissions for distribution.
    -   Code: are provided and can be executed for Editors to re-run and reproduce the published results
    -   Reproducible: with the provided code and data, the AER should be able to obtain results that match those claimed to be reproducible by the author
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    
    -   I think the main criticism is that the "reproducibility" idea behind Peng's proposal would potentially encourage "method-driven" analyses and unintentionally discourage the "problem-driven" analyses, which is much more complicated but substantive. The work, insights and thoughts behind those "problem-driven" analyses should actually be favored by the journals since those efforts open new paths for methodological research.
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    -   The commentary made by DeAngelis and Fontanarosa (2010) speaks to me the most. They talked about the potential danger of data manupulation, selective reporting of results, and inappropriate data analysis induced by the lack of independent academic statistical analysis, which highly appriciates the reproducibility of the original research.
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    -   For the commentary of DeAngelis and Fontanarosa, Keiding might believe they have different points of view: Keiding was talking about more about the directions in academic, but he thinks the "independent academic statistical analysis" defined by JAMA is a "pure auditing activity".
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

-   When the package (or some softwares) get updated, the previous "working" code becomes no longer working. 
-   More importantly, one might be really want to actually re-run and check the results again before he or she decides to distribute the code and data and claim the results are reproducible.  


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
