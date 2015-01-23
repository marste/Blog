---
title: Responsive YouTube and Vimeo Videos
author: Stefano Marzorati
layout: post
permalink: /responsive-youtube-vimeo-videos/
comments: true
categories:
  - Varie
tags:
  - responsive
  - youtube
  - vimeo
  - videos
  - css
---

`
.video-responsive{
    overflow:hidden;
    padding-bottom:56.25%;
    position:relative;
    height:0;
}
.video-responsive iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
}
`
