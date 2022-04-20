---
author: "Bufei Guo"
title: "Blog 7: Licenses"
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

*license* command in `R` will display the license under which `R` operates. `R` is distributed under GNU General Public License(GPL), either version 2, June 1991 
or version 3, June 2007. A small number of files are distributed under the LESSER GNU GENERAL PUBLIC LICENSE(LGPL).

`ggplot2` is under MIT license, which is stated on this website [MIT License](https://ggplot2.tidyverse.org/LICENSE.html).
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

**MIT**
1. Yes. Code can be freely copied, modified, and published.
2. Yes. It allows any person obtaining a copy of this software to deal in the software witout restrictions, including sell copies of the software
3. Nobody(or be at the users' own risk). The software is procided without warranty of any kind, thus neither the author nor copyright holders shall be hold 
responsible. 

**GPL-3**
1. Yes, but when publish the modified work or bundle with other code, the modified version or complete bundle must also be licensed with the GPL.
2. Yes, but with some restictions. The licensed materials and derivatives may be used for commercial purpose, but the same freedoms should be passed to the users,
i.e. users should have access to the source code of those derivatives and can change the software ot use pieces of it in new programs.
3. Nobody(or be at the users' own risk) to the extent permitted by applicable law if not otherwise stated. Users should check if the software does what it promises
to do, and should do corrections by themselves if necessary. 

**LGPL-3**
1. Yes. LGPL-3 has one excemption compared with GPL, if a larger work using the work through interfaces provided by the work i.e. use the work as a library,
 the larger work can be distributed without source code
2. Yes, but with some restrictions. The users should have asscess to the source code of those derivatives, except the case when the work is used as a library
in the derivatives.
3. Nobody(or be at the users' own risk) same as that of GPL-3

**CC-0**
1. Yes. Without conditions.
2. Yes. It can be used for commerical purposes.
3. Nobody(or be at the users' own risk) the license states that it does not provide any warranty 

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**
One consideration is that if my graduate work depends on others work and to what extent should my work depends on others. If the R package I use is under GPL-3,
then I should use the same license or similar license. Another consideration is if I want to incoporate data in my packages.

