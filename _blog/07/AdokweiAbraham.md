---
author: "Abraham Adokwei"
title: "Licensing in R"
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
  - *R* is licensed under *GPL-2|GPL-3* and *ggplot2* is licensed under *MIT* license. 
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
  - MIT
    - Yes
    - Yes
    - It is not too clear except that the authors or copyright holders cannot be held liable to any extent. In this case the license does not protect the person the who makes copies of the software. 
  - GPL-3
    - Yes, provided modifications are released under the same license and changes made to the licensed material, license, and copyright notice are documented. Also, the source code must be made available when the licensed material is distributed.
    - Yes
    - Unless required by applicable law or agreed to in writing, the copyright holder, or any other party who modifies it cannot be held liable for any sort of damage. 
  - LGLP-3
    - Yes, provided modifications are released under the same license and changes made to the licensed material, license, and copyright notice are documented. Also, the source code must be made available when the licensed material is distributed.
    - Yes
    - Unless required by applicable law or agreed to in writing, the copyright holder, or any other party who modifies it cannot be held liable for any sort of damage. 
  - CC-0
    - Yes
    - Yes
    - Unless required by applicable law or agreed to in writing, the copyright holder, or any other party who modifies it cannot be held liable for any sort of damage. 
3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
  - While working on my Master's Critical Component, I came across a project that will potentially lead to creating as R package. This package will essentially help individuals compute *BIC Values* when performing Principal Component Analysis for situations where $n\,<\,p$ by making reference to a paper by Bai et al 2018. Using *BIC* is one way to assess the number of components to retain. 
  - Looking over the three fundamental questions, I believe my closest option would be the *MIT License*. This is because, I want others to freely use my package without reservation plus I wouldn't have to deal with legal issues.  

Bai, Zhidong, Kwok Pui Choi, and Yasunori Fujikoshi. 2018. “Consistency of AIC and BIC in Estimating the Number of Significant Components in High-Dimensional Principal Component Analysis.” The Annals of Statistics 46 (3): 1050–76.

