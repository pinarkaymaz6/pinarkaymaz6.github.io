---
title: "How to set up static websites with Github Pages"
date: 2020-06-28
tags: [github pages, jekyll, static website]
header:
  image: "/images/githubpages/gh_pages.png"
excerpt: "GitHub Pages, Jekyll, Static Websites"
mathjax: "true"
---

I was considering creating a profile page or a blog for myself for a while. However, I was puting this idea off basically because creating content for your projects is not the easiest task and having to set up a website makes you procrastinate even more. Not any more!

It took me a couple of minutes to set up a profile with [GitHub Pages](https://pages.github.com/). You can have your website _freely_ hosted on GitHub’s `github.io` domain or on your custom domain.
> GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website.  

I started looking for a minimalist theme ideas for my profile page and came across this open source theme by [DataOptimal](https://github.com/dataoptimal/dataoptimal.github.io) which was built on top of the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes). In the following are the steps that I followed to deploy a version of it myself.

- Navigate to `dataoptimal.github.io` repository [here](https://github.com/dataoptimal/dataoptimal.github.io) and fork this repo.

![alt]({{ site.url }}{{ site.baseurl }}/images/githubpages/fork.png)

- Go to your repositories, the repo you just forked must have been added on your GitHub profile. You now have your own copy of the repository and can customize the files. 


- It's time to change the repo name. Go to `Settings` in your repo and edit repository name as seen below. The repo name should follow the convension and it should be your GitHub handle followed by `github.io`. Mine is `pinarkaymaz6@github.io`. 

![alt]({{ site.url }}{{ site.baseurl }}/images/githubpages/reponame.png)

- If you rename your repo correctly, go check your website. It should be up and running shortly on `your-username@github.io`. 

- Now you can customize your website and publish content in `Markdown` format. There are two main methods to edit the files: you can clone this repository on your machine or directly edit the files on the GitHub dashboard. Either way, your changes will be deployed once you save your changes on the dashboard or push it from your local copy to the remote master branch. 

- Go to the `_config.yml` file and replace the `author` attributes with yours. 
  - Replace the names and the images. 
  - Add your social media accounts.
-  You can also change the skin of the website by updating `minimal_mistakes_skin` on top of the config file. Mine is `dirt`. 
- To create a post, navigate to the `_post` folder and create a `Markdown` file following the naming convention `YYYY-MM-DD-<URL-PATH>`. 
- Now, push your changes to `master` branch and go check your website. It might take a minute to deploy, then try hard refreshing (`cmd + shift + R`) to see your changes.

This is all. I hope this was helpful. 

