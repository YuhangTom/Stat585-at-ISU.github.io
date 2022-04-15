---
author: "Mohammad Fili"
title: "Liscences"
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

**R**:    

Based on [this link](https://www.r-project.org/Licenses/), "R as a package is licences under `GPL-2 | GPL-3`. (it is under a Copyleft license)

In their website, it is also mentioned that the following licences are in use of R or associated software such as packages:

* The “GNU Affero General Public License” version 3
* The “Artistic License” version 2.0
* The “BSD 2-clause License”
* The “BSD 3-clause License”
* The “GNU General Public License” version 2
* The “GNU General Public License” version 3
* The “GNU Library General Public License” version 2
* The “GNU Lesser General Public License” version 2.1
* The “GNU Lesser General Public License” version 3
* The “MIT License”
* The “Creative Commons Attribution-ShareAlike International License” version 4.0


**ggplot2**:    
MIT (it is under a Permissive license)







2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

**MIT**:   
1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work? Yes (but the license must be preserved)

2. Are you and your collaborators fine with other people making a profit from those derivations? Yes (but the license must be preserved).

3. Who is responsible if your software does not do what it promises to do? There is no liability/warranty for software/packages used under this license.


**GPL-3**:    
1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work? Yes (["if you publish modified versions or bundle with other code, the modified version or complete bundle must also be licensed with the GPL"](https://r-pkgs.org/license.html))

2. Are you and your collaborators fine with other people making a profit from those derivations? Yes ["if you publish modified versions or bundle with other code, the modified version or complete bundle must also be licensed with the GPL"](https://r-pkgs.org/license.html)

3. Who is responsible if your software does not do what it promises to do? There is no liability/warranty for software/packages used under this license.



**LGPL-3**:   
1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work? Yes, but the source code should be made available unless it is a new program (a larger work using that software/package dynamically). In this case, it can redistributed under different terms.

2. Are you and your collaborators fine with other people making a profit from those derivations? Yes, but the source code should be made available unless it is a new program (a larger work using that software/package dynamically). In this case, it can redistributed under different terms.


3. Who is responsible if your software does not do what it promises to do? There is no liability/warranty for software/packages used under this license.




**CC-0**:   
1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work? Yes (but trademark and patents are not waived)

2. Are you and your collaborators fine with other people making a profit from those derivations? Yes (but trademark and patents are not waived)


3. Who is responsible if your software does not do what it promises to do? There is no liability/warranty for software/packages used under this license.




3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

Assuming that I am planning to create a Machine Learning Package for a specific project related to my research. One of the important things is the university policies. Because I am employed as an RA, and therefore, the license should comply with the policies of university. The other thing is if the project contains data and if that's the case, we need to know if data can be shared (under which terms?). Other considerations are: what is the scope? (Is that package going to be used by public, or it is specific to a very limited group of people?). And at last, personal preferences: Do I want to share the source code, or not? Do I want to allow aother to make profit of it, or not?



<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
