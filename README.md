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
### Embed Google Drive 

Embedding Google Drive videos have additional steps. 

1. For the desired video, change the link sharing setting to `On - Anyone with the link`. This will make the video accessible to anyone who has the link as no sign-in is required. 
  
  **Important**: If you do not change the video setting to this option, your video will not show.
  
2. Double click the video to show the preview. Click the setting options and select "Open in new window". Now click on the setting option again and select "Embed item". The iframe code should appear. For example:

```
<iframe src="https://drive.google.com/file/d/1EC8BnjJMon-vqy-UhLKk9sf_oukZzEbP/preview"></iframe>
```

`1EC8BnjJMon-vqy-UhLKk9sf_oukZzEbP/preview` would be your video ID.

**Note**: Right clicking the video will not bring up the embed option. You must open the video in a new window. 

Create a file in your `_includes` folder called `googleDrivePlayer.html` with this code inside: 

```
<div class="embed-container">
  <iframe
      width="640"
      height="480"
      src="https://drive.google.com/file/d/{{ include.id }}"
      frameborder="0"
      allowfullscreen="">
  </iframe>
</div>
```

Place this snippet inside your .md file where you want to embed your video:

```
{% include googleDrivePlayer.html id=page.driveId %}
```

On the top of your .md file, put the Google Drive video ID. You could also put the ID of the video directly.

```
---
driveId: putYourIDHere
---
```



### Installing in your local

```
bundle install
bundle exec jekyll serve
```

### Contributing

Feel free to [open a bug](https://github.com/myanmarpeopletaskforce/myanmarpeopletaskforce.guithub.io/issues) or [contribute to code](https://github.com/myanmarpeopletaskforce/myanmarpeopletaskforce.guithub.io/pulls)!
