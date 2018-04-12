---
layout: page
title: Blogging instructions
permalink: /how-to/blogging-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## 1. Fork the repository

Fork a copy of the organization [blog-posts](https://github.com/dig-eg-gaz/blog-posts) repository on your personal github account. Do this by clicking on the "fork" icon on the top right. You will be offered the chance to fork the repository under your own username--do so. This will make a copy of the repository in your own GitHub account, in which you should save your draft blog posts.

## 2. Name your post

Paste this [default text](https://raw.githubusercontent.com/dig-eg-gaz/blog-posts/master/YYYY-MM-DD-post-name.md) into a text editor (such as Atom) and save it with a unique name following this format: `2016-09-01-yourlastname-post-name.md`. Plug in today's date and a distinctive name for your post.

## 3. Fill in the header

The header (the material in the opening lines of the document, between the two --- lines) is very important. It tells the website how to treat your blog post. Enter your name (in quotation marks) as the subheadline. Give your post a title and provide a one to two sentence teaser. Enter the date and your name. Use the category "curiosities" for post 1, "technical" for post 2, and "serial questions" for post 3. List a few tags that reflect the subject matter that your post covers. Enter the name of an image that you would like to appear to promote the post on the header, thumb, and homepage lines, and give that image a caption and (if appropriate) a link. (For more on images, see number 5 below.)

## 4. Write a post in markdown and add images

You will write your text using [Markdown](https://en.wikipedia.org/wiki/Markdown), a very simple markup language but a different one from xml, which you are using for the newspaper pages. Here's a [tutorial](http://www.markdowntutorial.com/) and here's a [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Aim for at least 200 words, but it's fine if you write more. Integrate some links into your post, and use an image or two.

## 5. Working with images

Include an image clipped from your issue of the paper, and any other images that might add to the impact of your post. If you are using an image that you find on the internet, make sure that you have the right to reuse it, and download the image (don't just link to it). To include images in your post, add a line in the following format: `![Image label](image-file-name.png)`. Save these images in the forked folder. Make sure that you give all of the images a distinctive name, and use that name in the header and body.

## 6. Send a pull request to the group repository

When your blog post and image are ready, you can fold them back into the organization content repository by sending me a **pull request**. You do this by clicking the "new pull request" button the top left above your list of files. I will then see the pull request and either merge your files into the organization's content or request that you change something before doing so.
