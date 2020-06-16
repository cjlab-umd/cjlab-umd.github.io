![Computational Journalism Lab](./assets/images/logo.png)
This repository is for maintaining the website of the Computational Journalism Lab of the University of Maryland.

## Follow these steps to add a new project
+ Create a new html file in the `_posts` directory.
+ Add the following front matter.

```
---
layout: project
header:
  teaser: /assets/images/example.png
classes: wide
title: "Title of the Project"
date: 20XX-XX-XXT00:00:00-04:00
categories:
  - Computational Journalism
  - Another Category
tags:
  - Clickbait
  - NLP
short-name: a short descriptive phrase, for example, 'big-project'
---
```
+ Add relevant images in the `assets/images/` directory. The image names should start with the `short-name`. For example, `big-project-1.png`.
+ Use imagemagick to resize the images to 960x540 resolution by following the command. Note that it will change the aspect-ratio.
```
convert "big-project-1.png" -resize 960x540! -quality 100 "big-project-1.png"
```
+ If the aspect-ratio needs to be preserved, then use the following command to crop from the center.
```
convert "big-project-1.png" -resize 960x540^ -gravity center -crop 960x540+0+0 "big-project-1.png"
```
