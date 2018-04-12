---
layout: page
title: Regular expression instructions
permalink: /how-to/regular-expression-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---
Regular expressions (regex) is a very useful means of working with serial data which repeats similar information using similar formats.

[Regexr](https://regexr.com/) is a great place to learn about and try out regular expressions.

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## Using regex in Oxygen

You can use regex in the Find/Repace in Files tool when you enable the Regular Expression option in it. 
Some examples of commonly used regex codes:
- Search `\d+ \w+ \w+ ` for patterns like "100 tons cotton"
- Search `\W\w+ \W\w+ ` for personal names
- Search `at [A-Z]\w+ ` for locations (Remember to enable Case Sensitive)

## Using regex in Atom

To put `<persName>` around passenger names in a list: find `Mr. [A-Z][a-z, 0-9]+,` replace with `<persName>$&</persName>`.

<!-- To convert `<p>Budapest, January 4.</p>` to `<dateline>Budapest, January 4.</dateline>`: find `<p>[A-Z][a-z]+, [A-Z][a-z]+ [0-9]+\.<\/p>` and replace with `<dateline>$&</dateline>`. -->

## Cleaning XPath results

1. Select all, copy, and paste results into atom text editor.

2. Open find and replace. Click the Regex option, then use this line to remove some of the results:
Find `XPath location: .+\nStart location: .+\nEnd location: .+\n\nSystem ID: `
Replace with (leave empty). Click Replace All.

3. Remove the file location that precedes the issue date:
Find `/Users/whanley/GitHub/DEG-content/` (this will be different on your computer--just select everything that comes before the date filename)
Replace with (leave empty). Click Replace All.

4. Find `.xml\nDescription: `, Replace with `\t`. Replace All.

5. You'll have a bit of garbage left over at the beginning and end of the file. Delete this. Now you will have a tab-separated, two-column table that you can paste into a spreadsheet.

Recipe to clean `count` results, giving a single column response: `\n.+\nDescription: `

## Using regex in Microsoft word

Say you are trying to make a table of the results that you exported from Oxygen.

Import these results into a Word document. Then use Edit > Find > Advanced Find and Replace.

1. Find two paragraph marks (^p^p), and replace with @@.
2. Find one paragraph mark (^p), and replace with comma.
3. Find @@, and replace with paragraph mark (^p).
4. Select all text, then use Table > Convert > text to table.
