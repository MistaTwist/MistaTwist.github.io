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

I then opened a new command prompt - make sure you open one with ruby! - and installed the jekyll gem using the command:

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

I then created a new Jekyll site:

```bash
jekyll new ppblog
```

Then, change into the directory created for the new site, and do a test serve:

```bash
cd ppblog
bundle exec jekyll serve
```

In my browser, I opened up https://localhost:4000 and voilá!

## 2. Setup Github

First, you need to have a repo made, in case you need to. In order for it to work with github pages, you need to name it YOURUSERNAME.github.io

https://github.com/MistaTwist/MistaTwist.github.io

You need to ensure that it's not initialised with a readme.