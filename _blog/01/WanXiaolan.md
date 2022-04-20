---
author: "Xiaolan Wan"
title: "How to multiply matrices"
layout: post
topic: "01"
short-topic: Asking Good Questions
due-date: 2022-01-27
root: ../../
---

## Prompt:

Asking good questions is a valuable skill to have - asking questions in an online setting is both easier and harder than asking questions in person: we can prepare to ask a question but we are also expected to prepare.
The links posted here give some advice on how to ask good questions:

- stackoverflow's [Asking a good question](http://stackoverflow.com/help/how-to-ask)

- R's [Posting guidelines](https://www.r-project.org/posting-guide.html)

- [minimal complete verifiable example](https://stackoverflow.com/help/mcve), [minimal reproducible example](https://www.tidyverse.org/help/)

Follow these links and read through the advice given, then

1. **Pick at least one question from stackoverflow or the R help and answer it.**

Write a blog post answering the following questions: 

2. **Document which question you answered (link to your answer).**

3. **Relate your experience of answering the question to your reading. **


My blog: https://stackoverflow.com/questions/70816733/how-to-multiply-these-matrices


I help this person to do matrix multiplication in R. He needs to use the symbol `%*%` to do the matrix multiplication, rather than `*`.
Then I give an example and show him the correct function. 


This is my first time to answer other's questions on Stackoverflow. The website is very convenient to post my answer because I can insert my code there and it will automatically generate a clean code block. Thus, I can include my code to allow others to reproduce the results. Besides, I can create an example to better illustrate the question.


<!--Go to [https://github.com/Stat585-at-ISU/blog](https://github.com/Stat585-at-ISU/blog) for instructions about how to prepare and submit your blog post.-->
Instructions to follow.


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


