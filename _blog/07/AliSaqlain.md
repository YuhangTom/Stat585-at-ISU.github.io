---
author: "Saqlain Ali"
title: "License for Package"
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

     R operates under the GNU General Public License. The license for ggplot2 is MIT License(2020).

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

     MIT: It grants any person who obtains a copy of the software and associated files the right to use, copy, modify, merge, distribute, publish, sublicense, and             sell copies of the software. The only condition required to use the software is to include the same copyright notice in all copies or any substantial               portions of the software.
     
     GPL-3: Anyone can copy, modify and distribute this software but have to include the license and copyright notice with each and every distribution. You can use             this software privately or for commercial purposes. The software author or license can not be held liable for any damages inflicted by the software.
     
     LGPL-3: Like GPL, LGPL imposes no conditions on using the code in software that’s sold commercially. Users can rework the code, but if they distribute these                modifications, they must release these updates in source code form. It does not allow contributors to be held liable for legal issues or damages.
     
     CC-0: Licenses may copy, distribute, display, perform and make derivative works only if they give the author or licensor the credits. It may be copied,                    distributed, displayed, performed the work and make derivative works only for non-commercial purposes.

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
     
     Considerations that come into play in deciding on a license are the following:
     
     i) An exclusive license is more valuable to the licensee than a non-exclusive license because it enables the licensee to invest in the technology without               others benefiting from the investment. So, should we limit the exclusivity to a certain market or limit the value of my company to potential investors or           purchasers; are some things we should consider.
     
     ii) There are many options for the licensor to receive compensation for a license. We may decide to offer the license for a fixed license fee, a royalty                based on revenue generated using the technology or a combination of both.
     
     iii) A licensee may want to modify the technology, so determining which party owns the modifications and the rights of use are important to consider.
     
     iv) When license agreements do not generate anticipated revenues, unhappy licensors may wish to terminate the agreement. We can do this through availing a              shorter term which is generally better for the licensor since it preserves future options or to provide for a right to terminate early if specified minimum          revenue is not received.
     
     v) The licensee will want the licensor to have liability if the technology does not perform, or if a claim is brought against the licensee based on use of the         technology. Licensors can limit this risk by including limitations of liability.
     


<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
