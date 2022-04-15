---
author: "Danyang Zhang"
title: "Licensing"
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
GPL. MIT + file LICENSE.

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
**MIT**: The MIT license is a permissive license, and therefore people can modify the work, share the modified work, make a profit from those derivations, and are responsible for their own software.
**GPL-3**: The GPL license is a copyleft license. It allows people to freely modify the code, share the modified work, and make a profit from those derivations, and people are responsible for their own software.
**LGPL-3**: The LGPL license is a copyleft license. It allows people to freely modify the code, share the modified work, and make a profit from those derivations, and people are responsible for their own software.
**CC-0**: The CC-0 license is a permissive license, and therefore people can modify the work, share the modified work, make a profit from those derivations, and are responsible for their own software.

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
How to license your package depends on how you want people to treat it. If you just want people to keep the copyright and license notice, you can use the MIT license. Contributors provide an express grant of patent rights using the Apache license. If you want all derivatives and bundles of your code are also open source, choose the GPLv3 license. CC0 license puts minimal restrictions if your package primarily contains data, not code. License compatibility should also be taken into considerations when you are bundling other's code into your package.

<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
