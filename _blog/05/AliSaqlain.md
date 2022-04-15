---
author: "Saqlain Ali"
title: "renv"
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

1. **What is the idea of the renv package?**

The only way to be certain that the code written by someones else will run on our machine and will produce the same results is to replicate their environment. Using 'renv', we can create and manage project-local R libraries, save the state of these libraries to a 'lockfile', and later restore our library as required. Together, these tools can help make our projects more isolated, portable, and reproducible.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

Initially, installed the package ‘renv’. Then initialized the environment and installed all dependencies required for that R project. Finally took a snapshot of all the libraries used in that environment and all of the libraries got saved in ‘renv.lock’.

When I am trying to knit the Rmarkdown file it works perfectly fine but throws an error in ‘render-rmarkdown’ file in github. The following error is showing in github:

File ide-publish.png not found in resource path
Error: Error: pandoc document conversion failed with error 99


 

Submit this blog post to the blog-5 repo. 

