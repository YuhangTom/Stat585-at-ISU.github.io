---
author: "Mohammad Fili"
title: "Blog #5"
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

I used `install.packages('renv')` to install it.

2. **In the project for blog 3, initialize the workflow used by the `renv` package.**

I used the command `renv::init()` to initialize the r environment. Then I used `renv::snapshot()` to take a snapshot of the current environment (not necessary since I didn't make any changes to the packages). It created the `renv` folder with all packages needed to run this project, and the renv.lock file that has the description of all packages installed for this project.


3. **Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).**

All dependencies are listed.

4. **Add the `renv` folder to your blog 3 repository, and push the changes.**

I pushed the `renv` folder & renv.lock file.

5. **Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!**

Yes. After pushing the final changes, the github action worked without any problems/errors.


Write a blog post addressing the following questions: 

1. **What is the idea of the `renv` package?**

This package creates a private environment for a project and keeps all the packages and their dependencies there. So it is easy to maintain, manage, and debug when updating packages or modifying the code. Users can go back and forth between different versions of the environment without any concern.
Furthermore, if the user needs to run the code on a new machine, there is no worry about the R version, packages installed, and the existing dependencies between them.


2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

I found this packages a great tool that I can use in different projects. Recently I was looking for something similar for python to make sure that the user will use exactly the same versions of packages as I did to avoid any errors. Now, I know how to do it in R. This package was really easy to work with and the workflow was not complicated. I used it for Lab #3, and it worked perfectly fine.

 

Submit this blog post to the blog-5 repo. 

