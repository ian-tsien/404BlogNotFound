---
title: personal hexo best practices
language: en
date: 2025-07-10 22:31:17
categories:
- miscellanea
tags:
- Hexo
cover: /gallery/covers/hexo.png
thumbnail: /gallery/covers/hexo.png
---

The following is how the official site describes Hexo:

> Hexo is a fast, simple and powerful blog framework. You write posts in [Markdown](http://daringfireball.net/projects/markdown/) (or other markup languages) and Hexo generates static files with a beautiful theme in seconds.

Compared to other static site generators such as Hugo or Jekyll, Hexo strikes a nice balance between speed and simplicity. And unlike traditional CMS platforms like WordPress, Hexo can be deployed for free on GitHub Pages, with minimal maintenance.

Below are some personal best practices I've developed with Hexo, designed to help you set up a clean and efficient blog quickly—so you can focus more on writing, not tinkering.

---

## Install

The [official installation guide](https://hexo.io/docs/#Installation) is straightforward and reliable. Hexo is lightweight, so just follow the instructions step by step and you're good to go.

---

## Deploy

I recommend using [GitHub Actions](https://docs.github.com/en/actions) to deploy your blog to GitHub Pages. It works for both public and private repositories and is more modern than traditional "one-command" deployment approaches. It also aligns better with standard CI/CD workflows and reduces reliance on your local environment.

If you choose GitHub Actions, follow the [official deployment guide](https://hexo.io/docs/github-pages). Here’s one tip: you don’t need to stick to the `username.github.io` naming convention. A custom repository name, such as `404BlogNotFound`, gives you a cleaner and more meaningful URL like `https://ian-tsien.github.io/404BlogNotFound/` instead of the verbose `https://ian-tsien.github.io/ian-tsien.github.io/`.

> :warning: This works for me, but your mileage may vary.

---

## Theme and Plugins

Aesthetics are subjective. I use the **[hexo-theme-icarus](https://github.com/ppoffice/hexo-theme-icarus)**, which is elegant and highly customizable. There are many forks and variations of this theme, but unless you’re a hardcore Hexo user, I suggest sticking with the basic version for simplicity.

Here are two quick ways to get started:

- Switch to the [`site` branch](https://github.com/ppoffice/hexo-theme-icarus/tree/site) of the theme repository and copy the configuration files `_config.yml` and `_config.icarus.yml`. Then, replace the personal information with your own.  
  > Note: Some fields and files like `_config.post.yml`, `deploy`, or `algolia` may be unnecessary or deprecated—especially if you’re using GitHub Actions and not [`hexo-algolia`](https://github.com/oncletom/hexo-algolia) for search.

- Alternatively, clone my [repository](https://github.com/ian-tsien/404BlogNotFound) and reuse the cleaned-up versions of `_config.yml` and `_config.icarus.yml`. I’ve already removed unnecessary parts, so it’s easier to adapt.

To learn what each plugin does and how to customize your theme, check out the [theme documentation](https://ppoffice.github.io/hexo-theme-icarus/).

### Recommended Plugins

To fully support Markdown features and emoji parsing, I recommend installing:

- [`hexo-filter-github-emojis`](https://github.com/crimx/hexo-filter-github-emojis)  
- [`hexo-renderer-marked`](https://github.com/hexojs/hexo-renderer-marked)  
- [`hexo-image-link`](https://github.com/cocowool/hexo-image-link)

Of course, you can browse the [official plugin list](https://hexo.io/plugins/) for more options—but in my experience, these are sufficient. After all, **your content matters more than fancy features**.

---

## Writing Process

Get familiar with Hexo’s command-line tools by reviewing the [command documentation](https://hexo.io/docs/commands). Here's a simple flow chart:

![writing process](personal-hexo-best-practices/hexo_writing_process.svg)

I recommend starting with drafts:

```bash
hexo new draft <title>
```

Add `source/_drafts/` to your `.gitignore` so you can work privately, revise at your own pace, and publish only when you’re satisfied.

---

## Reference

- [Hexo Official Website](https://hexo.io/)
- [Hexo Theme Icarus](https://ppoffice.github.io/hexo-theme-icarus/)
- [My Blog Repo Example](https://github.com/ian-tsien/404BlogNotFound)
