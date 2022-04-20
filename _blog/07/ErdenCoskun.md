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

R software is distributed under the terms of the GNU General Public License, either Version 2 or Version 3.

ggplot2 has the MIT license. 


2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?
MIT: Yes, other people can use, modify and share the modified work without any restriction. 

GPL-3: Yes, but other people who incorporate our code in their product must release their work as GPL-3 too. 

lpgl-3: Yes, but other people who incorporate our code in their product must license our code as lpgl-3 while they can prefer any other form of license (e.g., more restrictive one) for the larger work.

CC-0: Yes, they can use the data as they wish. 

2. Are you and your collaborators fine with other people making a profit from those derivations?
MIT: Yes.
GPL-3: Yes.
lpgl-3: Yes.
CC-0:Yes.

3. Who is responsible if your software does not do what it promises to do?
MIT: Licensor assumes no liability under MIT. A licensee who incorporates our code into their product may be liable for the product's failure.
GPL-3: Licensor assumes no liability under GPL-3. A licensee who incorporates our code into their product may be liable for the product's failure.
lpgl-3: Licensor assumes no liability under lpgl-3. A licensee who incorporates our code into their product may be liable for the product's failure.
CC-0: Licensor assumes no liability under CC-0. A licensee who incorporates our code into their product may be liable for the product's failure.


3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

Other people utilizing my program, modifying it, and then sharing the modified work would be OK with me, especially if it was for educational purposes. However, I would rather not be held responsible for any potential errors. Furthermore, I would like anyone who use my code to allow others to use theirs. As a result, gpl-3 appears to be a suitable option. 


