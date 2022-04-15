---
author: "Abigail Collins"
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

1. **What is the idea of the renv package?**

The idea of the renv package is to be able to create and manage the R library of your current project. You can save the current state of your project libraries, and restore the project back to this state later on. The goal of the package is to help isolate/store your R project and all of its dependencies that makes sharing your project easier (for example, pushing to Github). 

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
 Working with the "renv" package went smoothly. Initially, within blog 3, I needed to be sure to load the "plyr" package before "dpylr", followed by the "renv" package. After loading all of the libraries needed to run the code for the blog, I used the command "renv::init()" from the "renv" package which initialized a new project-local environment. I was then able to push my assignment to Github and render the file without any errors. 

Submit this blog post to the blog-5 repo. 

