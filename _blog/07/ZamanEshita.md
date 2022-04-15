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
 R is licensed as GPL-2, and most R packages are also GPL-2 or GPL-3(source: www.r-bloggers.com). The license for ggplot2 is MIT + file LICENSE.
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
 1. My collaborators and I are fine with other people modifying our work and sharing that. 
 2. My collaborators and I do not want other people making profit out of the derivations. We would like to make it open source and use copyleft liencese like GPL.
 3. At least two main developers will be responsible to make sure the code is doing what it is supposed to do, even after other people modified the code. They can be reached via email about any package related issues.

4. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
If I develop a package for my graduate work, I want to make sure other people can be benefitted from that work as well. I want to make the package open source and make the license less restrictive. I will put the MIT license for the package. I also would be happy if someone else wants to enhance the functionality of the package. I will also be open if someone bundles my code into their own package
