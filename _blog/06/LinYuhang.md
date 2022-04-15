---
author: "Yuhang Lin"
title: "Reproducibility for journals"
layout: post
topic: "06"
short-topic: More on reproducibility...
due-date: 2022-03-03
root: ../../
---

## Prompt:

In 2009 one of the associate editors of Biostatistics, Roger Peng, outlined a new policy of [reproducibility](https://doi.org/10.1093/biostatistics/kxp014) for the journal. 

This triggered a response from one of the other associated editors, Niels Keiding, and subsequently a large part of volume 11, issue 3 of Biostatistics was dedicated to a discussion of issues of reproducibility. 


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
    
        **Answer:**
        To partially solve the lack of time and resources to reproduce examples of scientific investigations,
        one possible approach is to use a minimum standard called "reproducible research",
        which makes the data sets and codes assessable to others' verifications and further analyses.
        I think Roger Peng has already made it clear in 3 different aspects,
        "data", "code", and "reproducible" respectively in Section 2.1, and I am not going to copy them here.
        
    2. **What are Keiding's main criticisms of the proposal?**. 
    
        **Answer:**
        People should not "reproduce" by conducting "alternative analyses".
        He suggested that people should not perform poorly informed reanalyses of the original data sets,
        which is not likely to benefit.
        Also,
        it takes more to make a decision in a real project than just checking the arithmetic result,
        which is not likely to be the case when handling just the data from repositories.
        
    3. **Which point in the commentaries speaks to you the most? Why?**
    
        **Answer:**
        I found the JAMA policies explained by DeAngelis and Fontanarosa interesting.
        In their first policy,
        they further require someone to take the responsibility.
        From my point of view,
        I would say this practice at least force someone in the team to answer follow-up questions directly,
        which is definitely going to benefit the reproducibility of the result.
        In their second policy,
        they ask for independent analyses performed by someone else outside the team.
        That would make the result to be reproducible at least once.

        
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    
        **Answer:**
        He illustrated again his purpose of mentioning JAMA policy,
        which is just to clarify the JAMA “independent academic statistical analysis” as a pure auditing activity with no academic attraction.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on data related aspects)? What would you do differently if you could go back in time?**

    **Answer:**
    The most interesting and maybe the easiest way for us to check reproducibility is simply to download others' work from the cloud (Google drive again at that time) and run it locally.
    It would at least tell us something if someone gets error messages,
    and we would put that in comments or report to remind ourselves.
    If I can go back again,
    I would definitely start version control first and avoid modifying the files directly without any copy.
    Good documentations are also necessary for the purpose so it would always be helpful to go through the checklist questions before submission of any kind.


Go to [https://stat585-at-isu.github.io/blog-2022/](https://stat585-at-isu.github.io/blog-2022/) for instructions about how to prepare and submit your blog post.


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
