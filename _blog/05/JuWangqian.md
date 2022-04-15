---
author: "Wangqian Ju"
title: "Package renv and github action"
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

It records the version of R and any R packages used in the project, and allows users to track different versions and go back to the previous state. This is useful because one important thing to ensure the reproducibility is having or keeping the same version of R or R packages used in the project. It can reduce the probability of losing the reproducibility due to change of versions.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
All things went well. And I was able to pass the github action with the `renv` set up.

`renv::init()` works nicely. It creates the `.Rproj` file and correctly makes my local project folder recognized by the RStudio with git. I manually installed the packages `plyr` and `dplyr` again to make sure that the dependencies were correctly established, and called `renv::snapshot()` to record the dependencies. Then I pushed the files created by `renv::init()` and was able to pass the github action.


