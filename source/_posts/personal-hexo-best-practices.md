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

Compared to other static site generators, such as Hugo or Jekyll, Hexo strikes a balance between speed and simplicity. Compared to traditional CMS platforms like WordPress, Hexo can be free when deployed on GitHub and is convenient to maintain.

Here are some personal Hexo best practices designed to establish a visually appealing and efficient pattern in a short amount of time. It will take you hours to clone an identically good-looking site, and you can continue blogging without interruption.

## Install

There is no problem with following the [official install guide](https://hexo.io/docs/#Installation) step by step since Hexo is such a simple software.

## Deploy

It is better to use [GitHub Actions](https://docs.github.com/en/actions) to deploy GitHub Pages, which works in both public and private repositories, than using a one-command deployment unless you don’t want your source code seen by the public, because it is more modern and conforms to the conventional project development model with less reliance on the local environment.

As a former, follow the [official deployment guide](https://hexo.io/docs/github-pages). But here is a tip you should follow: you can directly choose a suitable repository name instead of following the format of `username.github.io`, for the reason that the former one will generate a more readable URL like `https://ian-tsien.github.io/404BlogNotFound/` than `https://ian-tsien.github.io/ian-tsien.github.io/`.

> :warning: ​​It works for me, but I don't guarantee it will work for you either.
>

## Theme and Plugins

The definition of beauty varies from person to person. I chose **[hexo-theme-icarus](https://github.com/ppoffice/hexo-theme-icarus)** as my theme. There are ample variants of this theme, but if you are not an enthusiast of Hexo, you should not excessively concern yourself with the details of these. For a fast configuration, you can choose one of the following ways.<br/>

* Switch the branch of the repository to [`site`](https://github.com/ppoffice/hexo-theme-icarus/tree/site) and plagiarize two configuration files `_config.yml` and `_config.icarus.yml`, by replacing your personal information. Notice that there are some useless or deprecated files like `_config.post.yml` and fields in `_config.yml` like `deploy` since you have chosen [GitHub Actions](https://docs.github.com/en/actions) to deploy GitHub Pages, and `algolia` since you have chosen you won't use [`hexo-algolia`](https://github.com/oncletom/hexo-algolia) as your search plugin.
* Go to my [repository](https://github.com/ian-tsien/404BlogNotFound) and plagiarize my personalized configuration files `_config.yml` and `_config.icarus.yml`, by replacing your personal information. It is easier to accomplish your files because I have eliminated unnecessary content.

Read the website [articles](https://ppoffice.github.io/hexo-theme-icarus/) written by the plugin developer to get a quick overview of the plugins included in this theme and personalize your blog style. You need to install two additional plugins, hexo-filter-github-emojis and hexo-renderer-marked, to support parsing Markdown grammar. Besides the plugins mentioned above, you can also scan [Hexo plugins](https://hexo.io/plugins/) to choose your own,  but I think the ones listed are sufficient, as the content of your blog is more important than its appearance or functionality.

## Writing Process

You need to learn basic usage of Hexo commands on this [page](https://hexo.io/docs/commands). Here is a flow chart.

![](gallery/workflows/hexo_writing_process.svg)

You could write a draft first by using `hexo new draft <title>` and add `source/_drafts/` to your `.gitignore`, so that you could revise it locally, and publish it when you’re satisfied.

## Reference

* [Hexo official website](https://hexo.io/)
* [hexo-theme-icarus](https://ppoffice.github.io/hexo-theme-icarus/)
