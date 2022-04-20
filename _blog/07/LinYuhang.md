---
author: "Yuhang Lin"
title: "Licenses"
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

    **Answer:**
    With `license()`,
    we can see that `R` is using GNU General Public License, either Version 2, June 1991 or Version 3, June 2007.
    `ggplot2` uses `MIT + file LICENSE`,
    released in 2020 and has all ggplot2 authors as copyright holder.
    
2. **Answer the three questions listed above for the licenses: MIT, GPL-3, LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

    **Answer:**
    - MIT: A permissive license
      1. Yes.
      1. Yes.
      1. The authors would not be responsible for warranty of any kind.
    - GPL-3: A copyleft license
      1. Yes.
      1. No. It is for personal use.
      1. The authors would not be responsible for warranty of any kind.
      They need to mark the modified versions after changing.
    - LGPL-3: A copyleft license
      1. Yes.
      1. No. It is for personal use.
      1. The authors would not be responsible for warranty of any kind.
      They need to mark the modified versions after changing.
    - CC-0: A permissive license
      1. Yes.
      1. Yes.
      1. The authors would not be responsible for warranty of any kind.
    
3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

    **Answer:**
    Firstly,
    I would pay attention to the type of license I want to use by answering the 3 questions listed above.
    As it would be hard to change it later,
    I would think about it seriously.
    Secondly,
    I would also figure out the copyright holders,
    and my supervisor, as well as the university, may have some suggestions or policies on this part.
    Last but not least,
    I would check if I add any codes given to me or any codes I bundled in the package.
    If so,
    I need to think about license compatibility as well as how to include those codes in the packages.

