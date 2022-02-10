---
layout: post
author: Ghazal
title: "how-to-plot-log-and-first-difference-of-log-in-r"
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
I chose a recent question which I had the knowledge to ansewr it. Her is the link to my answer, https://stackoverflow.com/questions/71055863/how-to-plot-log-and-first-difference-of-log-in-r/71058704#71058704. My name is Ghsh.

3. **Relate your experience of answering the question to your reading.**
It was a great experience for me. I have never posted something. Also, I answered the question incorrectly at first. When I reviewd my code, I understood that I made a mistake. Then I edited my reply. So, I think that I should read the question carefully when I want to answer a question since it may be resulted in misunderstabnding for the person who are asking a question.

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
