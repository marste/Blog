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
Inserisci nel tuo file .css questo codice:
<pre><code>
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
</code></pre>

Quando vorrai postare un video, non dovrai far altro che aggiungere la classe <code>video-responsive</code> in questo modo:

<!-- HTML generated using hilite.me --><div style="background: #ffffff; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #007700">&lt;div</span> <span style="color: #0000CC">class=</span><span style="background-color: #fff0f0">&quot;video-responsive&quot;</span><span style="color: #007700">&gt;</span>
    <span style="color: #007700">&lt;iframe</span> <span style="color: #0000CC">width=</span><span style="background-color: #fff0f0">&quot;420&quot;</span> <span style="color: #0000CC">height=</span><span style="background-color: #fff0f0">&quot;315&quot;</span> <span style="color: #0000CC">src=</span><span style="background-color: #fff0f0">&quot;//www.youtube.com/embed/2GxWs54v2d0&quot;</span> <span style="color: #0000CC">frameborder=</span><span style="background-color: #fff0f0">&quot;0&quot;</span> <span style="color: #0000CC">allowfullscreen</span><span style="color: #007700">&gt;&lt;/iframe&gt;</span>
<span style="color: #007700">&lt;/div&gt;</span>
</pre></div>
