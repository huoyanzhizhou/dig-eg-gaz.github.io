---
layout: page
title: Embedding Visualization Tutorial
permalink: /how-to/embed-visualization-instructions/
author: Will Hanley
date: 2018-01-05
header:
  image_fullwidth: front-page.jpg
---
<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

If you are using tableau or google sheets for your visualizations, you will embed them some other way.

If you are using google charts or some other code, to embed data visualizations in your markdown github pages, you need to do two things.

## 1. Host the visualization

Perhaps the easiest thing to do is to post your code as a [gist](https://gist.github.com/), then render it using a link from [rawgit](http://rawgit.com/).

## 2. Embed the visualization

Place this bit of code in a markdown file, and your visualization should appear:

`<iframe src="your-rawgit-link" width="90%" height="400"></iframe>`
