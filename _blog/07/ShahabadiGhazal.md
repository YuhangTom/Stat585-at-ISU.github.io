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
The MIT and Apache licenses are the most common modern permissive licenses; older permissive licenses include the various forms of the BSD license. The most common copyleft license is the GPL which allows you to freely copy and modify the code for personal use, but if you publish modified versions or bundle with other code, the modified version or complete bundle must also be licensed with the GPL. The license for ggplot2 is MIT + file.
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
Question 1: If we use MIT and CC-0, we are fine. Just we expect that they preserve the license by including their own copyright statements. If we use GPL-3, we are fine under the condition that their modifying code should be published with the same license without making patent or copyright claims on the original software. If we use LGPL-3, we are fine even if their modifying code will be published with any other license under the condition that they cannot make patent or copyright claims on the original software.
Question 2: We are fine with that just if we use MIT and CC-0 since it allows people to add their copyright statements under preserving the license. For the other two licenses, we are not fine since our using licenses do not allow them to make patent or copyright claims on the original software.
Question 3: The copyright holder (or holders) are the people who own the underlying copyright on the code and are hence the only people who are allowed to choose (or later change) the license. There are three main cases: If you wrote the code in your own time, you’re the copyright holder. If you wrote the code for your employer, your employer is the copyright holder. If you wrote the code for contract work, you’re the copyright holder unless the contract specifically describes otherwise.
3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
I prefer to use something like an LGPL-3 license since it makes it easier to modify the code without being worried about the license, and also it prevents the follower researcher who wants to extend my research to make patent or copyright claims on the original software.


<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
