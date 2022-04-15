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
    
    The reproducibility statement encourages authors to include the dataset or code (or both) they used in their paper as suplementary files. A paper is considered (fully) reproducible if similar results can be obtained by the AER or other readers of the paper using the data and code given by the authors. A reproducible paper can help readers verify the published results and conduct reanalysis or alternative analyses.
    
    2. **What are Keiding's main criticisms of the proposal?**. 
    
    The notation "reproducible" get confused by conducting "alternative analyses" as mentioned by Peng. We should not encourage researchers to do so on old datasets with limited information and knowledge. A reanalysis on a certain dataset should be based on a full acknowledgement and good understanding of the substantial background of the dataset, not by simply implementing the code as technical tools provided by the authors. This "reproducible" statement misleads the researchers by encouraging them to perform a minimum amount of work, whereas in fact deeper understandings of the data and far more analysis are required.
    
    3. **Which point in the commentaries speaks to you the most? Why?**
    
    The commentary by Dr. Cox and Donnnelly reemphasized the importance of distinction between (1) the "data driven" research and (2) using data to illustrate performance of statistical methods. They state that the notation of reproducibility mentioned by Peng is reasonable for the former case, but not totally applicable for the latter case because it contains more complex consideration from both the statistical and subject perspective. Doing analysis or reanalysis on the latter case requires deeper understanding of the data and the research subject.
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
    Keiding agrees with their commentary and quoted "the proposals for Biostatistics are to be welcomed even though their name and objectives are misformulated". There are many purposes of publishing data in a research, and the major purpose should be to encourage formulation of new methods and investigations, instead of reprtition of the original analysis done by the authors.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

My first research project was done in collaboration with researchers from Lawrence Berkeley National Lab. The major problem about reproducibility is that we don't have the permission from them to release the real data (maize gene expression data) used in the paper. In the end we only submitted the data and code in the simulation study. 

I think this is a big issue in statistics research nowadays, since the interdisciplinary studies have become more and more general. Publishing the code either in R or on github is easy, but it's a different story with the dataset. A common example will be using the medical records from hospitals, where the data should obviously not be published publicly, thus the reproducibility becomes at least partly unavailable. I don't think there's anything we can do on this issue :(

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
