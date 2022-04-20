---
author: "Zirou Zhou"
title: "R license"
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

R as a package is licensed under GPL-2 | GPL-3. File doc/COPYING is the same as GPL-2.

ggplot2 is licensed under MIT + file LICENSE.

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

MIT: YES, and the part of the code under MIT should still be under MIT license. YES, and the author will not be responsible for abuse the software.

GPL-3: YES, and the software or modifications using GPL3-licensed code must also be under GPL-3. And start changes. YES, and the author will not be responsible for abuse the software.

LGPL-3: YES, the software or modifications using LGPL3-licensed code must also be under LGPL-3. And changes should be stated. However, applications using the library don't have to be under LGPL-3. YES, and the author will not be responsible for abuse the software.

CC-0: YES, YES, and the author will not be responsible for abuse the software.

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

Since we are planning to use the most basic functions in R to build the package and we will still keep it open to anyone wants to use or modify it, It's rational to keep the same liscense with the R, which is GPL-3.

