---
author: "Firstname Lastname"
title: "Title of your post"
layout: post
topic: "07"
short-topic: All that legal stuff...
due-date: 2022-03-10
root: ../../
---

## Prompt:

The `DESCRIPTION` file of a package contains the package's meta information. Most of the fields in this file are quite straight forward: author, version number, and a short package description. When you call `library(help="<package name>")` for  package `<package name>` you can see the contents of the `DESCRIPTION` file for that package (and some parts of the `NAMESPACE` file).

Read through the chapter on [licenses](https://r-pkgs.org/license.html) from Wickham's book on R packages. 

There are several important aspects to consider when choosing a license for your work. 
Three of the main questions to answer are: 

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?

2. Are you and your collaborators fine with other people making a profit from those derivations?

3. Who is responsible if your software does not do what it promises to do?


Write a blog post addressing the following questions: 

1. **Under what license does R operate? What is the license for ggplot2?**

R: copyleft (GPL)

ggplot2: permissive (MIT)

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

  - MIT: 
 
    1. Yes (must include copyright notice and permission notice in all copies or substantial portions of the software)
  
    2. Yes
    
    3. The user. The authors of the package provides no warranty on any aspect, and are not liable for any error or damage cause by the package.
 
  - GPL-3: 
  
    1. Yes (must include copyright notice and permission notice in all copies or substantial portions of the software, must provide source code)
    
    2. Yes
    
    3. The user.
  
  - LGPL-3: 
  
    1. Yes, must keep the library open source, including any modifications you make, and allow users to obtain the source, license and copyright information for the library.
    
    2. Yes
    
    3. The user
  
  - CC-0: 
  
    1. Yes
    
    2. Yes, subject to rights and any other laws or restrictions that may apply.
    
    3. The user

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

I did finished an R package previously for my research. It used GPL-3 license. It is a most commonly used license for R packages, I've seen many other packages of similar functions using GPL license. 

The only difference between GPL and MIT (that matters to me) is that GPL requires distributors of code that contain the GPL license to make their source code available, which I think is more reasonable? 


<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
