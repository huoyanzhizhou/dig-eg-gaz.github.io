---
layout: page
title: TEI-XML instructions
permalink: /how-to/tei-xml-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---

## Objective
These instructions guide you in transforming your plain text page files into a marked-up xml document that conforms to the standards of [TEI](http://www.tei-c.org) (the Text Encoding Initiative).

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## 1. Set up your XML editor
Download the full-function Oxygen XML Editor, which offers a [free 30-day trial](http://www.oxygenxml.com/xml_editor/register.html). After 30 days, you might find [ways](https://10minutemail.com/) to renew your trial access, or simply purchase Oxygen using their [academic and educational discount](http://oxygenxml.com/academic/)).

## 2. Create an xml file
Copy and paste [this template](https://raw.githubusercontent.com/dig-eg-gaz/boilerplates/master/empty-issue.xml) into a new document. **Important**: the new document will have `<?xml version="1.0" encoding="UTF-8"?>` as its first line, and it's also the first line of the template; delete one of them, otherwise your document will be ill-formed. Name this document using the date of the issue and an xml extension (YYYY-MM-DD.xml). (This document will eventually contain all of the pages of the issue, so it is not necessary to add the page number to the document name.) Save this document on your hard drive.

## 3. Fill in the header
Enter your name into the template (under `<editor>`), today's date (under `<edition>`, in text and numeric formats), and the issue date (under `<bibl>`, in text and numeric formats). (Currently, these areas have entries in the comment format (`<!-- -->`)--replace these with your text). Save your file.

## 4. Copy and paste templated material
In your xml document, the text of your issue itself (as opposed to just the header) starts like this:

![page-1-example](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/page-1-example.png?raw=true)

The masthead is the banner at the top of page 1, which contains the title of the newspaper, the number, date, number of pages, and price, and is flanked by two advertisements. Update the number, date, and number of pages.

Now you need to find the templates that correspond to the ads that appear in your issue. There are detailed template instructions [here](https://dig-eg-gaz.github.io/how-to/templating-instructions/). Following the indications there, copy the xml text of template you need.

Next, you must paste this text into the right place in your xml document. The two ads flanking the masthead go right after the title, date, and so on, and before the `</div>` tag that closes the masthead:

![masthead-xml-example](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/masthead-xml-example.png?raw=true)

Then insert the first ad in the first column after the masthead after the `<cb n="1"/>` tag in the advertising section division, and proceed inserting ads all the way to the end of the page.

## 5. Make sure that your document is well-formed
At the top right hand corner of your editing window in Oxygen, there is a square that will be either red or green. If it's green, your document is well-formed, which means that it conforms to TEI XML standards and will be searchable and useable. If it's red, the file contains errors that you must fix before you submit it. The errors appear as red lines on the right hand scrolling column. Click on a line to see the error described at the bottom of your editing screen.

One common error that prevents a well-formed document:
- doubled `<?xml version="1.0" encoding="UTF-8"?>` lines at the opening of the xml document.

## Resources
- “[A Gentle Introduction to XML](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/SG.html),” TEI Consortium.
