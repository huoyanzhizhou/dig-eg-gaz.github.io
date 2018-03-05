---
layout: page
title: Templating instructions
permalink: /how-to/templating-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---
## Objectives

While [elements](https://dig-eg-gaz.github.io/elements/) of the *Egyptian Gazette* were composed fresh each day, much of each issue consisted of templates reapplied with minor or no modifications from issue to issue. As we produce our marked-up version of the newspaper, we can save effort by reusing templates in our own work. We must remain alert to minor variations, however.

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## 1. Recurring elements

The first step is to determine if you are looking at something that is a template. Advertisements, tables, and other material that is not free text is probably templated. Check these indexes to see if you can find something identical or similar to what you want to find:
- The complete catalog of advertisements is [here](https://dig-eg-gaz.github.io/advertisements/).
- The complete catalog of financial tables and other boilerplates is [here](https://dig-eg-gaz.github.io/templates/).
- Further down on this page, there are a few other miscellaneous templates.

These indexes contain images of the templated items, links to TEI-XML documents representing the templated item, and (sometimes) a comment or two about the template. Once you've identified the relevant template, copy and paste its XML into your own file. **Important**: Only copy the material contained within the `<body> </body>` tags--the rest of the file should not appear in your issue file. To do so, select the text like this:

![copy-paste-example](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/advertisement-copy-paste.png?raw=true)

Paste only this portion of the text into your issue document.

Next, customize the template content to match your issue's content. Often there will be no changes. Sometimes dates, names, or numbers will have to be changed. Sometimes the changes will be more complex. As you become more familiar with TEI-XML, you will get better at customizing the template.

If you can't find a template that should be there, or if your version of an item is so different from the template that you think a new template is warranted, there are a few things you can do. First, you can search the [repository of already-encoded issues](https://github.com/dig-eg-gaz/content) to see if someone has already produced a version of the material. If you find it, or if you feel up to encoding it yourself, you can turn this into a new template so that everyone can save time. Upload the xml and an image of the element to the [advertisements](https://github.com/dig-eg-gaz/advertisements) or [boilerplates](https://github.com/dig-eg-gaz/boilerplates) repository, and send a pull request. Finally, if you can't find the material anywhere and it's too involved to reproduce it yourself, file an issue at the advertisements or boilerplates repositories, insert a `<!-- missing template -->` comment with a few details into your document, and move on.

## 2. Miscellaneous templates

### D. Municipality
Municipal tenders appear in a formulaic fashion; it is necessary to change dates and particulars of the project being tendered. Template is [here](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/municipalite-avis.xml)

![Municipalite Avis](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-images/municipalite-avis.png?raw=true)

### E. Claims against the estate
Change name, rank, post, and dates on the [xml template](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/claims-against-the-estate.xml).

![Claims against the estate](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-images/claims-against-the-estate.png?raw=true)

### F. Vade Mecum for the Homeward Bound
This full-page vacation advertising section features on the seventh page of many issues between December 1905 and April 1906. This example is from December 5, 1905. Variations from issue to issue appear to be minor. Individual ads are not given their own xml:ids, because they are consistently repeated. For the whole page: xml:id="deg-el-vmhb01" [xml text](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-text/vade-mecum.xml)

![Link to image](https://github.com/dig-eg-gaz/boilerplates/blob/master/boilerplates-images/vade-mecum.jpg?raw=true)

## 3. An overview of issue elements

For a general summary of recurring elements, see the tables [here](https://dig-eg-gaz.github.io/elements/). Early on in this project, I made [this table](https://docs.google.com/spreadsheets/d/118Zv13fpHfm67i1k0Sm79OThV4ApD-d1iccvrpw1iYU/edit?authuser=0), which lists items commonly present in issues of the *Egyptian Gazette*. For a given date, the page and column number are listed. [This powerpoint presentation](https://docs.google.com/presentation/d/1vMoj-5ktfUAsfXrEbQJqy8vSsKhYiVyGVIZZqefrJW0/edit?authuser=0) displays the content layout of several issues during the month of July 1905. (The main boilerplate is six pages long. On Wednesday and Saturday, when issues are eight pages, the extra pages are the fourth and fifth pages. Pages 6-8 of extended editions correspond to pages 4-6 of regular editions.)
