---
author: "Kieran Liming"
title: "What are Licenses"
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

R uses GPL-2 and GPL-3, parts of R are under each. ggplot2 Uses the MIT + file LICENSE this is a "permissive" license, meaning it is the only restriction is the license must be preserved. 

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

**MIT:**

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?

Yes, there are very few restrictions.

2. Are you and your collaborators fine with other people making a profit from those derivations?

Yes, the only stipulation is the license must remain

3. Who is responsible if your software does not do what it promises to do?

This is the important aspect of this license, the authors deny liability if the software does not work.

**GPL-3:**

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?

The GPL license allows coders to modify the code for personal use, but publishing the code must also come with the GPL license. In practice this means that all derivatives of the code also must remain open source. 

2. Are you and your collaborators fine with other people making a profit from those derivations?

In this case it is still fine to profit from someone else's code with a GPL3 license, however the code and its derivatives can not be made private.

3. Who is responsible if your software does not do what it promises to do?

Like the MIT license, the authors are not held liable.

**LGPL-3:**

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?

Yes, in this regard it is very similar to GPL-3.

2. Are you and your collaborators fine with other people making a profit from those derivations?

Yes, where this differs from GPL-3 is that the derivatives of the work can be licensed under a different license. Under GPL-3, the derivatives would need to be licensed under GPL-3 as well.

3. Who is responsible if your software does not do what it promises to do?

Just like the licenses above, the authors do not hold liability.

**CC-0:**

1. Are you and your collaborators fine with other people modifying your work and then sharing the modified work?

Yes!

2. Are you and your collaborators fine with other people making a profit from those derivations?

Yes! This is the license puts the data into the creative commons, meaning it can be used by anyone without fear of repercussion 

3. Who is responsible if your software does not do what it promises to do?

Not the Authors!

3. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**


In the case where I am working with code and data, it is likely drawing from public data to begin with. I feel a morale imperative to allow replication of my code in some capacity to enhance the field of statistics (and likely baseball). Therefore, a license like the GPL-3 license seems like a valid choice for me. It would allow adaptations of the work and would also require those changes and advancements to also be made public. This seems like the best collaborative license in that regard.  



