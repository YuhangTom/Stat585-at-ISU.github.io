---
author: "Alex Cleveringa"
title: "Blog 7: License to License"
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
R operates under GPL-2. The license for ggplot2 is MIT + file LICENSE.
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
MIT: Modifying the code and sharing it is okay. Profiting from those derivations is also okay. If the software doesn't do what it's supposed to do, the copyright holders are not responsible.
GPL3: Copying and modifying the code for personal use is okay. Derivatives of the code are also open source, which means that others can make a profit from the derivatives. Copyright holders are not responsible for any inability to use the program.
LGPL3: Anything you can do with a GPL3 license, you can also do with a LGPL3 license. That includes modifying and sharing the code, as well as profiting from the derivations. Copyright holders are still not responsible for any inability to use the program.
CC-0: modifying and sharing the data is okay, and so it profiting from the derivations. I'm not sure what data promise to do, but since CC-0 is an equivalent to the MIT license, the authors are not responsible for that.
3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
The project that I am working on is composed of data collected from the Iowa Soybean Association. Upon completion of the project, the data and code will be made publicly available for others to use through an R package. Therefore, we would be okay with people making modifications to the code and data. As far as I know, there is not an issue with someone making a profit from creating a tool that gives fertilizer recommendations to farmers that was trained with our data. In our scenario, I would consider using an MIT license.


<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
