---
layout: post
title: "Use jekyll for Github Blog"
description: "Quickstart for jekyll"
category: others
tags: [jekyll github]
---
{% include JB/setup %}

## Install jekyll at github.com
__1. create one repo__  
create the repo at [github](https://github.com) named USERNAME.github.com.  
__2. Install jekyll with git__

    $ git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com.  
    $ cd USERNAME.github.com  
    $ git remote set-url origin https://github.com/USERNAME/USERNAME.github.com.git
    $ git push origin master  
__3. check jekyll at github.com__  
check jekyll by access USERNAME.github.io  

## Install jekyll at local for md testing
Jekyll provide markdown syntax local check tools `jekyll --server` to preview your blog before push to github. it''s need more times   
_NOTE: before do the following steps, run `echo 'insecure' >> ~/.curlrc` for ca_  

    $ curl https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer | bash -s stable
    $ echo '[[ -s $HOME/.rvm/scripts/rvm ]] && source $HOME/.rvm/scripts/rvm' >> ~/.bashrc
    $ source ~/.bashrc
    $ rvm requirements  
    $ rvm install 1.9.2 && rvm use 1.9.2
    $ rvm rubygems latest
    $ gem install jekyll  

disable insecure mode of curl by delete insecure line in ~/.curlrc, then  

    $ cd USERNAME.github.com  
    $ jekyll --server

Now, check local jekyll by type `http://localhost:4000`, your blog is here.
## Custom Jekyll
__1. download and switch the template.__  
Here are the [templates](https://github.com/jekyllbootstrap).  
_Download Themes:_

    $ rake theme:install git="https://github.com/jekyllbootstrap/theme-the-program.git"  

_Install Themes:_  
If you type Y after download, the theme will auto install and switch. Also you can manual install.  

    $ rake theme:install name="THEME-NAME"
 
After download and install, you will find them in `./_theme_packages` folder.  
_Switch Themes:_  

    $ rake theme:switch name="the-program"

Check theme switch by restart `jekyll --server`.  
__2. change `_config.yml` for blog__  
_TODO_  
## Work with Jekyll
Some concept about Posts and Pages, pls follow Jekyll introduction in Referency.  
Here is a example for write one blog.  
__1. create post__

    $ rake post title="Use Jekyll For Github Blog" date="2013-4-20"

md file location ./_posts/2013-4-20-use-jekyll-for-github-blog.md  
__2. write blog__  
define the catagories and tags and write blog with markdown.  
## Reference
1. [Jekyll Quickstart](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)
2. [Jekyll org website](http://jekyllbootstrap.com/)
3. [Jekyll introduction](http://jekyllbootstrap.com/lessons/jekyll-introduction.html)
4. [Use Jekyll Theme](http://jekyllbootstrap.com/usage/jekyll-theming.html)
