---
layout: post
title:  "0. Installing Ruby and Jekyll"
date:   2021-09-17 01:00:00 -0700
categories: jekyll update
---

#  Installing Ruby
In conjunction to our usage of Github in this class, we are able to utilize GitHub pages as the host of our website through the usage of a static site generator named Jekyll. Because Jekyll is an installable Ruby Gem, first you would need to install Ruby.

Some relevant Ruby terminology would include:

1. Gems
    > A gem is a *Library* that you can install and call for usage in your projects or applications. New gems can be found amongst Ruby's open source gem community or through other third-party librarys. The term *gem* came purely out of the fact that it is a pun along side the term *Ruby*. lol

    >There are six components of a gem including: `README`, `lib`, `spec/test`, `Executable`, `gemspec`, and `Rakefile`.

2. Gemfiles
    >Your gemfile is a file that lists the gems that the user is using in their project. Alongside the bundler, the gemfile is able to install, update, manage, and review the project's gems.

3. Bundler
    >Bundler is another Ruby gem that is used to manage the packages and dependencies for your application through the usage of *gemfiles*.

<br />

# Installing Jekyll

![alt text](/images/jekyll-image.png)

After the installation of Ruby, run the following commands in order to install Jekyll, create a new site, and to double check that Jekyll has been prperly installed. The steps to install jekyll are actually quite simple and are as follows:
```
$ gem update
$ gem install jekyll bundler
$ jekyll -v
$ bundle update
$ jekyll new <Name of your page>
$ cd <Name of your page>
```
# Final Look
In order to view my GitHub Pages site as I was making changes I was able to use the following command within the GitHub Page repository:
``` 
$ bundle exec jekyll serve 
```
This command helped to locally (http://localhost:4000/) view the changes I was actively making rather than having to `git push` and publish my edits. This reduces the number of `commits` that are made to the repository and also reduces the need to switch back and forth between your terminal, IDE, and web browser.

<html><head><link rel="stylesheet" href="style.css"></head></html>