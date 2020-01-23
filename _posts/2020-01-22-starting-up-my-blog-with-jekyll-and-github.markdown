---
layout: post
title:  "How to build a blog on Jekyll and Github pages"
date:   2020-01-22 16:31:39 +0000
categories: jekyll github
---

## 1. Setup Ruby and Jekyll
In order to install Jekyll you'll need to first get your dev environment cooking with Ruby.

I'm on a windows machine, so I grabbed the recommended installer [HERE][ruby-installer], ran it, and chose the default options (pressed enter instead of choosing a particular option) and let it do it's thing.

[ruby-installer]: https://rubyinstaller.org/downloads/

I then opened a new command prompt - make sure you open one with ruby! - and installed the Jekyll gem using the command:

```bash
gem install jekyll bundler
```

Once that had completed, I checked we were all good by checking the version of Jekyll:

```bash
jekyll -v
```
I then fired up Visual Studio Code, and in the terminal, navigated to my projects folder where I was going to get up my blog folder:

```bash
cd documents/projects/blog
```

I then created a new Jekyll site, called "ppblog":

```bash
jekyll new ppblog
```

Then, change into the root directory created for the new site, and do a test serve:

```bash
cd ppblog
bundle exec jekyll serve
```

In my browser, I opened up https://localhost:4000 and voilá! You'll see a placeholder post, all ready to re-purpose.

![Initial Post View](/assets/img/InitialServeView.png)

From here, you can edit your first post and such, which I'll leave up to you for now. Plenty of documentation can be found on the Jekyll site here.

## 2. Setup GitHub Pages to host your Jekyll site

First, you need to have a repo made, in case you need to. In order for it to work with GitHub pages, you need to name it YOURUSERNAME.github.io

https://github.com/MistaTwist/MistaTwist.github.io

You need to ensure that it's not initialised with a readme.

Next, in the terminal, back in your project's root folder (in this example it's ppblog), do the following:

```bash
git init
```
This initialises your project as a git repo.

If youve made any changes, you can commit them, along with a message, via the source control section in the VSCode side-navigation.

Next, we run the following commands:

```bash
git remote add origin https://github.com/MistaTwist.github.io.git
git push -u origin master
```

The above commands do the following:

- Adds a remote git repo (target to push code to) called "origin" to your project. It's like an alias.
- Pushes your local code to the master branch of the repo and adds an upstream association to our newly added remote "origin".

And there you go - if you now browse to your repo in GitHub, and browse to the Settings tab, scrolling down you'll see the GitHub Pages section, where the link to your site will be.

![GitHub Pages view](/assets/img/GitHubPages.png)

Now I'm ready to blog, and so are you :)