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
 renv package is used to manage the R package dependancies in a project. It is a stable replacement of Packrat package. When renv is installed and activated in a project, it can crawl through the project script to find the package dependencies and install them. It can store the snapshot of the packages at a given time and store it in a renv.lock. User can restore a previous state of project from renv.lock. User can also define which folders/files to scan for package dependencies of the project. Tt stores the source and version of downloaded R packages. renv can also save the downloaded packages in a global cache, in that case the downloaded packages can be shared among the projects using renv. This saves package downloading overhead. 

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
My experience of working with renv is great. I installed the package and initialized the environment with renv::init(), installed the necessary R packages. I run the script and pushed the renv folder in Git repo. I have also noticed that all the Git actions passed in the repo.

Submit this blog post to the blog-5 repo. 

