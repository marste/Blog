---
title: Slideshow3
date: 2017-02-15 11:42:00 +0200
author: Stefano Marzorati
layout: slide
theme: white
transition: slide
published: true
permalink: /slideshow/
categories:
  - Fun
tags:
  - sempre
  - qualcuno
  - prezzo
  - basso
---
<section data-markdown>
## Esempio 1
</section>

<section data-markdown>
# Esempio 2
</section>

<section data-markdown>
# Esempio 3
</section>

<section data-markdown>
## Slide Layout

Create a layout file, call `slide.html` in `_layouts` folder. And use this gist
for the content of the file https://gist.github.com/luugiathuy/c07ac5608addadb642e5.

</section>

<section data-markdown>
## Slide

Now, in your page/post YAML front matter, use `slide` for the layout. You can
define *title*, *author*, *description* as well as the slide's *theme* and
*transition*:

```yaml
---
layout: slide
title: Jekyll&#58; Make presentation page with reveal.js
description: A presentation slide for how to use reveal.js in Jekyll
theme: black
transition: slide
---
```
</section>

<section data-markdown>
## Slide

Each slide is enclosed in a `&lt;section&gt;` tag:

```html
&lt;section data-markdown&gt;
## Overview

[reveal.js](https://github.com/hakimel/reveal.js/) enables you to create
beautiful interactive slide decks using HTML. This presentation will show you
how to integrate it with [Jekyll](http://jekyllrb.com/)
&lt;/section&gt;
```

</section>

<section data-markdown>

# THE END

</section>