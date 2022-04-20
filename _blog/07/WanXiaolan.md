---
author: "Xiaolan Wan"
title: "license"
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
 
 R is licensed under General Public License, either Version 2, or Version 3. The license for ggplot2 is MIT license.
  
  
2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

**MIT**

    1. Yes, work can be modified and shared, as long as the original MIT license is included.

    2. Yes, work can be used for commercial purpose, as long as the original MIT license is included.
    
    3. No, the author of the work is not responsible for not working.
    
**GPL-3**

    1. Yes, work can be modified and shared, as long as you preserve the orginal licences and copyright and state the modifications.

    2. Yes, work can be used for commercial purpose, as long as you preserve the orginal licences and copyright and state the modifications.
    
    3. No, the author of the work is not responsible for not working.


**LGPL-3**

    1. Yes, work can be modified and shared, as long as you preserve the orginal licences and copyright and state the modifications.

    2. Yes, work can be used for commercial purpose, as long as you preserve the orginal licences and copyright and state the modifications.
    
    3. No, the author of the work is not responsible for not working.


**CC-0**

    1. Yes, work can be modified and shared.

    2. Yes, work can be used for commercial purpose.
    
    3. No, the author of the work is not responsible for not working.




3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

If I am in the process of making a package, I would like to allow my work to be shared and modified. But in the mean time, I prefer others to include the original licence and copyright, and state the midifications. In this way, others can add some new features to my package and I can also see these changes.



