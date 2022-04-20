---
author: "Parastoo Akbari"
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

1. **Under what license does R operate? What is the license for ggplot2?** The official R software environment is an open-source free software environment within the GNU package, available under the GNU General Public License. The license for ggplot2 is MIT + file LICENSE.  
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**
MIT: 
first question : yes / second question : yes / third question : the authors will not be responsible.
GPL-3:
first question : it's okay if they want to modify codes for their personal use, but if they want to share it, the modified version must also be licensed with GPL. / second question: yes / third question: there is no warranty for this free software.  For both users' and authors' sake, the GPL requires that modified versions be marked as changed, so that their problems will not be attributed erroneously to authors of previous versions.
CC-0:
first question: no, only copyright holders have the right to do so. / second question: no / third question: the authors will not be responsible. 
3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.** My graduate work does not contain data. The first thing that should be considered is that whether I want to let other easily change, copy and share my codes. If so, then I have to choose a permissive license such as MIT or Apache; otherwise, copyleft licenses would be better. In my work, I think that would be okay if others can easily use my codes, so I prefer permissive license. Another thing, that should be considered is that if I want to bundle someone else's codes into my own packages, I should be careful about license compatability. 


