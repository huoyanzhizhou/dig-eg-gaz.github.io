---
layout: page
title: Serial question instructions
permalink: /how-to/serial-question-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---
Your final project is to consider a theme or question that recurs across many issues of the *Egyptian Gazette*

Part of your work is to compose a serial question that makes sense and can be answered by the dataset. Explain this question (supplying, for instance, the xpath formula you will use), and explain how you extract the results. For guidance on queries, consult the [tutorial](https://dig-eg-gaz.github.io/how-to/query-instructions).

To consult previous serial analysis projects, see this [directory](https://dig-eg-gaz.github.io/analysis/analysis).

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## How do I submit material?

Fork the [analysis](https://github.com/dig-eg-gaz/analysis) repository, add your analysis and images, and send a pull request. Do this at least twice: once you've finished your question, and a second time once you've written your analysis. It is fine to do it more often too, sending partial material or drafts. I will make comments, and you can revise them.

Make sure that *every* file name starts with your name (so that we don't get confused by a whole bunch of `graph.jpg` files), and that you have no spaces in your file names--use dashes instead.

## How do I format my serial analysis?

Write it in markdown.

Use a header:

```
---
layout: page
title: <!--- insert title --->
author: YourName
---
```

Name it something like `yourname-analysis.md`.

## What about images?

Please produce data visualization(s) to accompany your analysis.

You may use a variety of tools:

- [Palladio](http://hdlab.stanford.edu/palladio/)
- [Google charts](https://developers.google.com/chart/)
- [Tableau](https://dig-eg-gaz.github.io/how-to/visualization-instructions/)

## How do I show these visualizations in my markdown page?

If you are using google charts or some other code, to embed data visualizations in your markdown github pages, you need to do two things.

1. Host the visualization: Perhaps the easiest thing to do is to post your code as a [gist](https://gist.github.com/), then render it using a link from [rawgit](http://rawgit.com/).

2. Embed the visualization: Place this bit of code in a markdown file, and your visualization should appear:

`<iframe src="your-rawgit-link" width="90%" height="400"></iframe>`

If you are using tableau or google sheets for your visualizations, you will embed them some other way. Details to come.
