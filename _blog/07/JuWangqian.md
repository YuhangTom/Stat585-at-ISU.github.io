---
author: "Wangqian Ju"
title: "Discussion on Licenses"
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

    -   `R` has `GPL-2 | GPL-3`, and `ggplot2` has `MIT + file LICENSE`

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

    -   All four licenses give permissions to modification, distrivution, and commercial use. But they are under different conditions. And the copyright holder should be responsible for the code.
    -   MIT: requires license and copyright notice
    -   GPL-3: requires that source code must be made available; a notice of the copyright and the license itself; using the same license for all released modifications; documenting changes made to the licensed materials
    -   LGPL-3: requires that source code must be made available; a notice of the copyright and the license itself; documenting changes made to the licensed materials. Additionally, it requires using the same license for all released modifications but this one may not apply to "works that use the licensed material as a library"
    -   CC-0: no condition specified.

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

    -   I think it's important to achieve an agreement on which license to use among all the contributors. At the same time, understanding my funding source and it's potential impact is also crucial. 



