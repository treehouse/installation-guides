---
layout: page
title:  "Installing Jekyll on Mac"
date:   2015-05-27
categories: mac
---

## What is Jekyll?
[Jekyll](http://jekyllrb.com/) is a blog-aware static site generator powered by Ruby. A static site generator takes a set templates and raw text files, runs it through a converter and renderer, then generates a plain HTML website that's ready to publish on any web server.

The blog-award part means that blogging is part of Jekyll’s functionality. We can publish and maintain a blog by simply managing a folder of text files. 

With Jekyll, we can build a blog, a portfolio, or any website that has a series of post entries without having to depend on a database or content management system. That's because Jekyll doesn't require setting up a complex application on a web server like WordPress, Ruby on Rails, or Flask. Instead, all the development magic happens on your computer. When Jekyll is done, it gives you a set of regular web pages that you can upload to any server. 

**The installation process is very straight forward:**

1. The best way to install Jekyll is via [RubyGems](https://rubygems.org/pages/download). In your Terminal prompt, simply run the following command to install Jekyll on your Mac:

        gem install jekyll

    This command automatically installs all of Jekyll’s gem dependencies. That's it!

2. To create a new Jekyll project, run the following command:

        jekyll new project-name


## Known installation issues
There are currently no reported issues.  If you are having one, please report it in the [Treehouse forum](https://teamtreehouse.com/forum/q:jekyll).