## Description

> This project forked and has been modified from https://agusmakmun.github.io,
> and the search posts using [Super Search](https://github.com/chinchang/super-search)

#### Features

* Sitemap and XML Feed
* Pagination in homepage
* Posts under category
* Realtime Search Posts _(title & description)_ by query.
* Related Posts
* Highlight pre
* Next & Previous Post
* Disqus comment
* Share on social media
* Google analytics
* HTML Minify _(Compress HTML)_ using [Jekyll Compress HTML](https://github.com/penibelst/jekyll-compress-html)

### Install & Configuration

1. Fork this repository
2. Edit site settings inside file of `_config.yml`
3. Edit about yourself inside file of `about.md`

### How to Use?

**a. Add new Category**

All categories saved inside path of `category/`, you can see the existed categories.

**b. Add new Posts**

* All posts bassed on markdown syntax _(please googling)_. allowed extensions is `*.markdown` or `*.md`.
* This files can found at the path of `_posts/`.
* and the name of files are following `<date:%Y-%m-%d>-<slug>.<extension>`, for example:

```
2021-02-01-welcome-to-jekyll.md

# or

2021-02-01-welcome-to-jekyll.markdown
```

Inside the file of it,

```
---
layout: post                          # (require) default post layout
title: "Your Title"                   # (require) a string title
date: 2021-02-01 19:51:02 +0800       # (require) a post date
categories: [socialpunishment, boycott]          # (custom) some categories, but makesure these categories already exists inside path of `category/`
tags: [foo, bar]                      # (custom) tags only for meta `property="article:tag"`
image: Broadcast_Mail.png             # (custom) image only for meta `property="og:image"`, save your image inside path of `static/img/_posts`
---

# your content post with markdown syntax goes here...
```


#### Installing in your local

```
bundle install
bundle exec jekyll serve
```

### Contributing

Feel free to [open a bug](https://github.com/myanmarpeopletaskforce/myanmarpeopletaskforce.guithub.io/issuess) or [contribute to code](https://github.com/myanmarpeopletaskforce/myanmarpeopletaskforce.guithub.io/pulls)!
