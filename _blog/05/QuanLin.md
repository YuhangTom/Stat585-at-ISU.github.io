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

`renv` package is a great package to bring local R project dependency management to the projects. It helps us create reproducible environments for the R projects. First, `renv` could make the R projects more isolated. `renv` package give each project its own private package library. So Installing a new or updated package for one project won’t break the others. Second, `renv` could make the R projects more portable. It easily transports the projects from one computer to another, even across different platforms. `renv` makes it easy to install the packages the project depends on. At last, `renv` could make the R projects more reproducible. `renv` records the exact package versions our depend on, and ensures those exact versions are the ones that get installed wherever we go.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

I'm not familiar with `renv` package, but the document "Introduction to renv" helped me alot. The command is simple, I just use `renv::init()` and `renv::snapshot()` to fix the error in blog 3. Since this is my first time using this package, I tried to add arguments in `renv::init()`, I add project and bare, which is not correct. It took me a lot of time to figure out that I should do.

Submit this blog post to the blog-5 repo. 

