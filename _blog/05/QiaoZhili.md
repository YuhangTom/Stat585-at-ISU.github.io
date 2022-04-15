---
author: "QiaoZhili"
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

I think the `renv` package works by recording the library dependencies of your R package into a single lock file. If you encounter problems with packages later, you can simply restore to previous (successful) versions from this lock file. This can also be used to solve the github problem we encountered in blog 3, by uploading this good-to-run library dependency into github, and tell github to follow this guide instead of trying to figure out what packages to use and how to use by itself.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
To be honest, I don't know. My code already worked originally in Blog 3 (thanks to the help from Will!). Adding the code from `renv` package doesn't seem to change anything, except for extra running time for initializing and writing the .lock file. Anyway it didn't produce any error...


Submit this blog post to the blog-5 repo. 

