---
author: "Gabrielle Collins"
title: "R Licensing Intro"
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
R operates under a GPL2 license and ggplot2 operates under a "MIT + file" license.

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
MIT: 1. Yes 2. Yes 3. The maintainer/user is responsible. The creator is not liable under a MIT license.
GPL-3: 1. Yes, but all derivatives of the code must also be open source with GPL-3 licensing 2. Yes 3. The person using the package is responsible and the creator isn't liable.
LGPL-3: 1. Yes, but source code must be made available, a copy of the license and copyright notice must be included with license material and in most cases the same type of license, or a similar license must be used when distributing the material. 2. Yes 3. This license provides no warranty over it's code so the user is fully responsible.
CC-0: 1. Yes 2. Yes 3. This license provides no warranty over it's code so the user is fully responsible.

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

My creative component deals with modeling handwritng data and I use the data that is made publically available on the CSAFE website. When making a package for this model, I would need to consider the limitations on the data that I am using, and how publically available I want to make this model when deciding on a license. The fact that project relies on other code written by members of CSAFE, would also need to be considered when choosing a license, as I would need to awknowledge this contribution.  

