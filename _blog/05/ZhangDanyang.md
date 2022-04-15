---
author: "Danyang Zhang"
title: "Get to know the renv package"
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

1. Install the R package `renv` on your local machine.
2. In the project for blog 3, initialize the workflow used by the `renv` package.
3. Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).
4. Add the `renv` folder to your blog 3 repository, and push the changes.
5. Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!


Write a blog post addressing the following questions: 

1. **What is the idea of the renv package?**
The renv package helps with project-local R dependency management. Projects using renv will use a per-project R library, and the R dependencies are isolated from other R libraries on the system, so that any of the existing workflows should just work as they did before even uf there are changes to the packages.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
All attempts of mine went well. I initialized a new project-local environment with a private R library using init(), installed plyr and dplyr packages,used snapshot() to save the state of the project library to the lockfile (called renv.lock), called to the dependencies() function to implicitly add all dependencies to the environment, added the `renv` folder to my blog 3 repository, and pushed the changes. The github action worked regardless of the sequence of loading `plyr` and `dplyr` packages, and I can safely load both packages.

Submit this blog post to the blog-5 repo. 

