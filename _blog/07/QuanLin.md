---
title: "license"
author: "Firstname Lastname"
layout: post
topic: '07'
short-topic: All that legal stuff...
due-date: '2022-03-10'
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

<ul>R as a package is licensed under GPL-2 | GPL-3. Some header files are distributed under LGPL-2.1. </ul>
<ul>ggplot is licensed under MIT + file LICENSE.</ul>

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

<ul>
 	  <li><b>MIT</b>: 1. and 2. Yes. Other people can modify the work and share the modified work.T hey should include the copyright and license notices in the work. There is no restrictions on copying, modifying, merging, publishing, distributing and commercial use of it. 3. No one is responsible if the software does not do what it promises to do. The author or copyright holder should not be liable for any situation.</li>
 	  <li><b>GPL-3</b>: 1. and 2. Yes. GPL-3 is a free and non-profit software. Other people can copy,modify and distribute the software. But they should state changes, disclose source code, include the copyright and license notices. Other people can use the work commercially. 3. There is no warranty. The modified version has to be marked as changed. So the authors of previous versions are not responsible for any problem.</li>
    <li><b>LGPL-3</b>: 1. LGPL-3 allows everyone to copy and distribute copies of the license document. But changing it is not allowed. Other people can copy, distribute and modify it under the same condition as GPL-3. The applications using the library don't have to be under GPL. 2. Yes, Other people can use the work for commercial purpose. 3.No warranty. The authors or copyright holders are not responsible if the software does not do what it promises to do.</li>
 	  <li><b>CC-0</b>: 1. and 2. Yes. CC-0 releases software into public domain. This license allows everyone build upon, enhance reuse the work for any purpose. There is no restriction under copyright ir database law. 3. No one is responsible if the software does not do what it promises to do.</li>
 	</ul>

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

<ul>If the package is created by myself, I would use GPL-3. First, I can share with others. Then, since the modified version of GPL-3 is required to be marked as changed, I can keep my rights. If the version has been modified by others, I'm not responsible for the modified one. If I basically use the functionality from other packages, I will follow their licenses.</ul>

<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
