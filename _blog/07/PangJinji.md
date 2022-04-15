---
author: "Jinji Pang"
title: "Aware of different types of licenses"
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

- R is licensed as GPL-3.
- ggplot2 uses "MIT + file LICENSE".

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

- MIT:
  1. yes, distribution and modification are allowed, but a copy of the license and copyright notice must be included with the licensed material.
  2. yes, commercial use is allowed, but a copy of the license and copyright notice must be included with the licensed material.
  3. nobody


- GPL-3:
  1. yes, modification and distribution are allowed, but the new work should also using the same license. 
  2. yes, commercial use is allowed but new work should disclose original code source, use same license and state changes.
  3. nobody


- LGPL-3:
  1. yes, modification and distribution are allowed, most of time the new work should use the same license, but in some cases, the new work can also use a similar or related license. If the licensed material was used as a library, then this same license condition is exempted.
  2. yes, commercial use is allowed. Four conditions must be met,  disclose source code, include license and copyright, same license (most of the cases), and state changes.
  3. nobody

- CC-0:
  1. yes, modification and private use are allowed. It's similar to unlicense, so no conditions are required.
  2. yes, commercial use is allowed. No conditions are required.
  3. nobody


3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

First of all, I think the most important thing I want to make sure is that I, as the author, are not responsible if the code does not do what it promises to do. Because the only reason I choose to release my code it to help others, not gaining any profits, so I don't want to be involved in any troubles. 
Second, I still want to get acknowledgement for my work, so I probably won't choose CC-0 license, instead I will consider GPL or LGPL because those two licenses require disclose source code.

