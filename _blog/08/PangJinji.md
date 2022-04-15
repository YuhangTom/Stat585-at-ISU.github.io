---
author: "Jinji Pang"
title: "Build personal website using GitHub Pages and Blogdown"
layout: post
topic: "08"
short-topic: Blogdown...
due-date: 2022-03-24
root: ../../
---

## Prompt:

GitHub is an incredibly useful tool for project management and collaboration. It also has several useful features for professional promotion: you can host your own site on github using [GitHub pages](https://pages.github.com/), describe yourself using a GitHub developer profile, and even use [resume.github.io](http://resume.github.io/) to generate a resume summary of your activity on GitHub (you must opt-in by [starring the project page](https://github.com/resume/resume.github.com)). 

RStudio and the associated package infrastructure provide multiple ways to generate websites using Rmarkdown. You can complete this assignment using one of two options: 

- Simple RMarkdown websites    
For more information about simple R Markdown websites, please read the documentation at https://bookdown.org/yihui/rmarkdown/rmarkdown-site.html. Simple R Markdown sites are _not_ based on **blogdown**. They are probably good for websites with only a few Rmd documents.

- [Blogdown](https://github.com/rstudio/blogdown)    
For larger-scale and more sophisticated websites (such as blogs), you may want to use **blogdown** instead: https://github.com/rstudio/blogdown.

## Instructions:

1. Create a new GitHub repository named `<your-username>.github.io` (replacing "<your-username>" with your GitHub username). Initialize this repo with a readme.

- My gitHub Page is `jinjipang.github.io`.


2. Set up your website using either the Simple Markdown Site or Blogdown instructions below. If you would like to use this repository to host a blog, you may find Blogdown to be a more convenient option, however, it is more complicated than the simple Rmarkdown site. 

- I used Blogdown to set up my GitHub Page.

3. Rename the <LastnameFirstname>`.Rmd` in your repo. Write at least 2-3 sentences describing the problems you encountered while following these instructions, how you solved them, and how you anticipate using this site in the future. 

- Actually I started using Blogdown from last summer and I've enjoyed writing blogs with it very much. However, while setting up my GitHub Pages, I still encountered several problems. First, in my previous website, I used `config.yaml` to set up my website's configuration, but this time, I got `config.toml`, there are some differences of syntax between `.yaml` and `.toml`,that's why I spent some time in figuring out how to set up the configuration of my new website. I used Yaml to Toml converter online tools. The second problem is I am not familiar with `html` syntax, so I couldn't make my Home page fancy, such as adding pictures on the header or footer. I am still learning how to modify the Home page by watching some YouTube videos.

- I feel this GitHub Page is very useful, it's free, stable, and convenient. I plan to use this site to document my academic projects and for showing my CV.



### Simple RMarkdown Site

1. Use RStudio and set up a new project on your machine linked to the GitHub repository you just created. 

2. Create two files in your project folder:
    - `_site.yml`:
      ```
      name: "my-website"
      output_dir: "."
      navbar:
        title: "My Website"
        left:
          - text: "Home"
            href: index.html
      ```
    
    - `index.Rmd`
      ```
      ---
      title: "My Website"
      ---
      
      Hello, Website!
      ```

3. Use the commmand `rmarkdown::render_site()` to build your website (Or click the "Build Website" button under the Build tab in RStudio). This command will compile any R markdown document in the main project directory to HTML (even if it is not mentioned in `_site.yml`). 

4. Push your site to GitHub. In this instance, you want to include the HTML files that were rendered, the `site_libs` directory, the `_site.yml` file used to configure the build process, and the Rmd files used to render the HTML files.

5. Customize your site. Remember to use the command `rmarkdown::render_site()` before you push your changes so that the HTML is updated!
    - Modify `_site.yml` to update the header structure, add links to other files, etc. 
    - Modify `index.Rmd` to add content to the landing page of your site. You might think about including a link to your CV on this page. 
    - Add new Rmd files to add new pages to your site. Consider adding a page describing your favorite packages, or pages for different projects you've worked on. 
    
### Blogdown

1. Install the `blogdown` package (`install.packages("blogdown")`)

2. Create a new folder where you will store the source for your blog and the rendered site.

3. Use RStudio to create a new project inside the folder you created in step 2. Select "blogdown site" as the project type, and name this project "source"

4. Use RStudio to clone your github repository (`<your-username>.github.io`) inside the folder you made in step 2 (NOT STEP 3!)    
At this point, from the directory you created in step 2, your file structure should look something like this:
```
├── source
│   ├── config.toml
│   ├── content
│   ├── index.Rmd
│   ├── public
│   ├── .Rhistory
│   ├── .Rproj.user
│   ├── source.Rproj
│   ├── static
│   └── themes
└── username.github.io
    ├── .git
    ├── .gitignore
    ├── README.md
    ├── .Rhistory
    ├── .Rproj.user
    └── username.github.io.Rproj
```

5. Open the "source" project. Edit source/config.toml and add the directive: `publishDir= "../username.github.io"`, modifying to include your username. This ensures that when you build your blog, it will update the directory associated with the git repository.

6. Open the "username.github.io" project. Add a text file named ".nojekyll" (the file should be empty). This tells GitHub not to build the pages with Jekyll (another rendering engine) and instead render pages built with Hugo (what blogdown uses).

7. Edit source/config.toml. 
    - Change the GitHub link to link to your github profile page. 
    - Add the correct twitter account if you have one (otherwise, delete the 3 lines from [[menu.main]] to the twitter URL). 

8. Build the site (from the source project) using `blogdown::build_site` or Ctrl-Shift-B    
At this point, from the directory you created in step 2, your file structure should look something like this:
```
├── source
│   ├── config.toml
│   ├── content
│   ├── index.Rmd
│   ├── public
│   ├── .Rhistory
│   ├── .Rproj.user
│   ├── source.Rproj
│   ├── static
│   └── themes
└── username.github.io
    ├── config.toml
    ├── content
    ├── .git
    ├── .gitignore
    ├── index.Rmd
    ├── public
    ├── README.md
    ├── .Rhistory
    ├── .Rproj.user
    ├── static
    ├── themes
    └── username.github.io.Rproj
```
    
9. In the "username.github.io" project, add everything that is in the folder to the git repository (you can leave .gitignore, .gitkeep, and .Rproj out if you choose, but everything else should be added.) Commit your changes, and push them to github. Check to make sure you can now load the site by going to "https://username.github.io" in a browser.

10. Make the site yours! Using the RStudio project associated with the source directory, 
    -  Consider adding a link to your CV or other interesting project pages by modifying the setup/config.toml file. [Here](https://bookdown.org/yihui/blogdown/configuration.html#toml-syntax) is a link to the page explaining toml syntax. 
    - Edit source/content/about.md to describe you.
    - Add new content (if you want) using `blogdown::add_content()`
    - Clean out the source/content/post directory to remove the default blog posts. 
    - use `blogdown::new_post()` to make a new post. You can set the YAML metadata to mark a post as a draft, to set the publication date, and more. 
11. Build the site from the RStudio project associated with the source directory. Commit changes using the username.github.io RStudio project. 



