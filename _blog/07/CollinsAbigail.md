---
author: "Abigail Collins"
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

R operates with open-source licenses, specifically GPL2. The license for ggplot2 is MIT.

2. **Answer the three questions listed above for the licenses: MIT, GPL-3,  LGPL-3, and CC-0. Note that some of the questions might not be answered with a simple yes/no. In that case, go into more detail, but do not just copy the terms of the license.**

MIT: As stated in chapter 9, the MIT license is a permissive license, which means that code with this license can be freely copied, modified, and published (as long as the license is preserved).

  1.) Yes. Under this license, you can your collaborators can allow others to modify your code and share it.
  2.) Yes. The description of the licsense states that selling copies of the software is allowed (ie commericial use is allowed). 
  3.) You are responsible to use the software at your own risk. The authors and copyright holders of the software are not liable for any issues with the software. 
  
GPL-3: The GPL-3 license is a copyleft license, which means that you can freely copy and modify the code for personal use, however if you want to publish anything, your publication needs to be licensed with the GPL.

  1.) Yes, others can modify and share your code, as long as they do so such that their modifications/sharings also use the same GLP-3 license. They also need to clearly state that they made modifications to the software.
  2.) Yes, as long as they too publish/modify/share code using the same GLP license so others can do the same.
  3.) As long as the conditions stated above are met, the author or copywriter of the software are not liable for any issues with the software package then. You use the software at your own risk. 
  
LGPL-3: This software is similar to the GLP-3 license, but has lesser restrictions.

  1.) Yes, under this license others can modify and share your work. Under this license, your entire “work” doesn’t have to have under this same license, you can use other licenses as well.
  2.) Yes, commerical use is allowed under this license. 
  3.) If the software does not do what is promised, the creator is at no fault. 
  


CC-0: The description of this software license states that license "waives copyright interest in a work you've created and dedicates it to the world-wide public domain", in other words, there are not many restrictions when using this license. It is typically used when your package is primarily data and not code.

  1.) Yes. As stated in the license description, the public can modify/incoporate/distribute, and reuse packages with this license as freely as possible in any form whatsoever.
  2.) Yes, commerical use is allowed under this license.
  3.) You are responsible, you acknowledge that, the software being used under this license in your "work" is being used as is. 




4. **Assume that you are in the process of making a package for your own graduate work. Describe considerations that come into play in deciding on a license. In case you are not quite at that stage in your graduate studies yet, come up with a likely scenario. Describe it and discuss.**

My graduate work entails the analysis of high school data from the state of Iowa (the dataset that I have is confidential). In my analysis, I am trying to predict first year college retention rates based on high school performance. The functions that I am creating may be useful to other educational research studies. However they would not be able to access my data. Therefore I think a GPL license would be appropriate, so other can use/modify/share any functions or code I write, but it must be applied to their own data and modified to fit the state of which they have data for. A GPL license would be good because they can make edits, but they must also use the same license so others, or myself, could use/check it. 


<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
