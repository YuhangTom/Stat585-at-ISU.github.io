---
author: "Zirou Zhou"
title: "Blog 05"
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

The `renv` package allows me to use `snapshot` to record the packages I used in the project and `restore` to reinstall the packages next time when I use this project. And it allows me to download package from different sources. The `lock` can make sure there's no conflict between collabrators.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

I performed the'renv' command in project blog 3 and it correctly reports the packages I'm using. When I pushed the folder to git, however, it was unsuccessful. Dr. Hoffman later discovered that the issue stemmed from access to the Rmd file and that a 'lock' document was missing. As a result, the'renv' package is up and running, but the file access needs to be checked.
 

Submit this blog post to the blog-5 repo. 

