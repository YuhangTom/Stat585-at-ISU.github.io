---
author: "Parastoo Akbari"
title: "Blog 5"
layout: post
topic: "05"
short-topic: Fixing github actions
due-date: 2022-02-24
root: ../../
output: github_document
---

## Prompt:

Remember the github action disaster of blog #3? :)
This week, we will try to tackle the cleanup, and you write a paragraph or two about your experience with it. 

Read the vignette [Introduction to renv](https://rstudio.github.io/renv/articles/renv.html) for the `renv` R package by Kevin Ushey.

Then do:

1. **Install the R package `renv` on your local machine.**

2. **In the project for blog 3, initialize the workflow used by the `renv` package.**

3. **Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).**

4. **Add the `renv` folder to your blog 3 repository, and push the changes.**

5. **Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!**


Write a blog post addressing the following questions: 

1. **What is the idea of the renv package?** This package helps to manage library paths and the existing workflows should just work as they did before. renv is a tools that helps to make projects reproducible by recording R + R packages being used in a project, and providing tools for reinstalling the outdated versions of those packages in a project (For example, like plyr and dplyr). 

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?** In Blog 3 I was not able to update codes on my repo and GitHub actions were not complete. It is because plyr, which is an old version. However, when I installed renv package in my local machine, and then installed both plyr and tidyverse packages, I didn’t get any errors, and my codes run without any problems. But I am not able to upload the renv folder on repo!
Submit this blog post to the blog-5 repo. 

