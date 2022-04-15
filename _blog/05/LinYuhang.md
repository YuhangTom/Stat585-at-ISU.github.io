---
author: "Yuhang Lin"
title: "Fix the failed github action for blog #3"
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

    **Answer:** Called `install.packages(renv)`. Done.

2. **In the project for blog 3, initialize the workflow used by the `renv` package.**

    **Answer:** Called `renv::init()` in the directory for blog 3. Done.
    

3. **Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).**

    **Answer:** After installing and updating packages, called `renv::snapshot()`. Done.

4. **Add the `renv` folder to your blog 3 repository, and push the changes.**

    **Answer:** Done.

5. **Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!**

    **Answer:** Yes, I finally get a green tick in "Actions"! No more errors and red crosses!


Write a blog post addressing the following questions: 

1. **What is the idea of the renv package?**

    The `renv` package is trying to create a "project-local environment with a private R library".
    It would record the state of the project library and try to isolate the project’s R dependencies.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
    
    Everything goes well for me even before I remember to modify the "render-markdown.yaml".
    I just followed the workflow listed on `renv` vignette and it works perfectly.
    I spent a lot of time trying to fix this unsuccessful action before blog 3 was due and failed.
    I never thought it would be such a simple fix.
    Anyway, I also modified the "render-markdown.yaml" as requested, tested it and it still works.

Submit this blog post to the blog-5 repo. 

