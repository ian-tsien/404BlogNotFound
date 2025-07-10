---
title: personal hexo best practices
language: en
date: 2025-07-10 22:31:17
categories:
- tools
tags:
- configuration
cover: /gallery/covers/hexo_cover.png
thumbnail: /gallery/covers/hexo_cover.png
---


The following is the definition given by official websites.

> Hexo is a fast, simple and powerful blog framework. You write posts in [Markdown](http://daringfireball.net/projects/markdown/) (or other markup languages) and Hexo generates static files with a beautiful theme in seconds.

Compared to other static site generators, such as Hugo or Jekyll, Hexo strikes a balance between speed and simplicity. Compared to traditional CMS platforms like **WordPress**, Hexo can be free when deployed on GitHub and is convenient to maintain.

Here are some personal Hexo best practices aimed at building an aesthetic and handy pattern in a short time. It will take you hours to clone an identically good-looking site, and you can keep blogging continuously.

## Install

There is no problem with following the [official install guide](https://hexo.io/docs/#Installation) step by step since Hexo is such a simple software.

## Deploy

It is better to use [GitHub Actions](https://docs.github.com/en/actions) to deploy GitHub Pages, which works in both public and private repositories, than using a one-command deployment unless you don’t want your source code seen by the public, because it is more modern and conforms to the conventional project development model with less reliance on the local environment.

As a former, follow the [official deployment guide](https://hexo.io/docs/github-pages). But here is a tip you should follow: you can directly choose a suitable repository name instead of following the format of `username.github.io`, for the reason that the former one will generate a more readable URL like `https://ian-tsien.github.io/404BlogNotFound/` than `https://ian-tsien.github.io/ian-tsien.github.io/`.

> :warning:
>
> It works for me, but I don't guarantee it will work for you either.

## Theme and Plugins

The definition of beauty varies from person to person. I chose **[hexo-theme-icarus](https://github.com/ppoffice/hexo-theme-icarus)** as my theme 

## Writing Process

* hexo new `quotation mark`
* hexo serve

## reference

[how to wirte a good technical article](https://www.freecodecamp.org/news/how-to-write-a-great-technical-blog-post-414c414b67f6/)

[hexo official website](
