---
author: "Danyang Zhang"
title: "More discussions about reproducibility"
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
    The framework has three dimensions to evaluate the reproducibility. Making the analytic data from which the principal results were derived available; providing any computer code, software, or other computer instructions that were used to compute published results; executing the code on the data provided and producing results matching those that the authors claim are reproducible successfully.
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    Keiding believes that "method-driven" research, which are reanalyses of old data sets, are detached from the original context. Moreover, stronger focus should be on "problem-driven" research, which always involves collaboration between statistician and substantive scientist. The work on the data set produced by these people's countless concrete judgments made in their course of a substantive study could be reproducible, but the real substantive context is ignored in Peng's proposal of reproducibility. 
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    The commentary made by D. R. Cox and Christl Donnelly speaks to me the most. In Peng's proposal, making sets of data available is one dimension of reproducibility. It makes sense to me when the commentary states that the transparency of data could inspire the formulation and investigation of new questions. We should not be too greedy to think about reproducibility as reproducing the whole process for every research, every effort towards replication: data, code, and the whole process, has its own value.
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    Keiding agreed with Cox and Donnelly's acknowledgement of the variety of purposes of making data available, and their conclusion that the proposals for Biostatistics are to be welcomed even though their name and objectives are misformulated. His main points are: reanalyses of old data sets detached from their original context run a risk of alienating the methodological developments from the problems they were intended to help solve, and close contact between the statistician and the substantive researchers is not assured during reanalysing.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**

There were a lot of randomnesses when building and explaining the model in a data intensive project. Each if we kept track of the random seeds used, variations in results made us confused about which version was telling the true underlying story. If someone rerun our work, he/she could come up with a different and even opposite result, if the same random seed is not used. What we did back then was that we tried a bunch of random seeds, recorded the results, and followed what the majority of results was showing us. I would propobably stick to this way, additionaly, state clearly what random seeds we have used, so that others could reproduce the same results.

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
