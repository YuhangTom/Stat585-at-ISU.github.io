---
author: "Firstname Lastname"
title: "Title of your post"
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

The renv is a tool that can help make projects reproducible by recording the version of R version and R packages being used in a project, and reinstalling the declared versions of those packages. For example, renv::snapshot() can save the state of the project to renv.lock; renv::restore() can restore the state of the project from renv.lock. Renv helps manage library paths to isolate the project's dependencies to ensure that the existing workfolws work as they did before.


2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

In my local R studio, I can easily initiate the workflow using the `renv` package  to generate a renv folder and a renv.lock file by `renv::init()`, and upload these files to my repository. However, I encountered with the Error: install of package 'curl' failed [error code 1]. I attempted changing the command `uses:r-lib/actions/set-up-renv@v1` to `uses:r-lib/actions/set-up-renv@v2`, and installing the `curl` package, but it still didn't work. 

 

Submit this blog post to the blog-5 repo. 

