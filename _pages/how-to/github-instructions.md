---
layout: page
title: GitHub instructions
permalink: /how-to/github-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---

## Objective
We will manage our digitization of the Egyptian Gazette using GitHub. This tutorial gives you instructions about how to submit your own work to our shared repositories.

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## 1. What is GitHub?
GitHub is a tool to manage versioning and collaboration in coding projects large and small. It's built on [git](https://en.wikipedia.org/wiki/Git) software, and offers a bunch of useful social and communication tools in its user interface. Each of us will create an individual account where we'll store and refine our work until it's ready to upload to the [dig-eg-gaz organization repositories](https://github.com/dig-eg-gaz).

## 2. How to access GitHub
You can approach GitHub three ways:
- using a web browser to access [github.com](https://github.com/),
- using the [GitHub Desktop](https://desktop.github.com/) client , or
- using [the command line](http://programminghistorian.org/lessons/intro-to-bash).

We'll be using the Desktop client mostly, but in a pinch you can use the web browser.

## 3. How to use the organization repository and your own fork of it
1. Create an account, and email me your username so that I can add you to the dig-eg-gaz organization..
2. Navigate to the organization [content repository](https://github.com/dig-eg-gaz/content), and **fork** the repository by clicking on the "fork" icon on the top right. You will be offered the chance to fork the repository under your own username--do so. This will make a copy of the repository in your own GitHub account.
3. Clone this repository in your Desktop.
4. In GitHub Desktop, right click the "content" repository, and choose "Show in Finder." This will show where the content files you've just cloned are stored on your hard drive. Move your xml files here, and continue to edit and save them in this location. Desktop will help you to send these edits to Github.
![show in finder](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/content-show-in-finder.png?raw=true)
5. When you're ready to sync your changes with the GitHub cloud, write a summary of your changes (e.g., "creating page 1"), hit "Commit to Master", then hit "Fetch origin" (on the top right). This will backup your work onto your fork on GitHub's servers.
![fetch origin desktop](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/fetch-origin-desktop.png?raw=true)

## 4. How to submit your deliverables
When your page files are complete, you can fold them from your own fork into the **master** organization content repository by sending me a **pull request**. You do this by clicking the "new pull request" button the top left above your list of files, following the instructions there. I will then see the pull request and either merge your files into the organization's content or request that you change something before doing so.

## 5. How do I make sure that my content fork is up to date?
When it comes time to do your querying and analysis of others' files, it's very important to make sure that you are working on an up-to-date version of the content files. When you look at your fork of the `dig-eg-gaz/content` repository on the github website, you will see a line comparing your repository to the organization repository:
![not up to date](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/250-commits-behind.png?raw=true)
If you are ahead, click the "new pull request" button above the status report and ask the organization to merge your changes.

If you are behind:

1. click "pull request" on the same line and to the right of the status of the report.
2. You may then be taken to a screen saying "There isn't anything to compare." Click on the "switching the base" link just below.
3. You will then be taken to a screen that allows you to create a pull request. Do so.
4. This pull request will now appear on the "pull requests" tab of your fork of the content folder.
![pull requests](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/pull-requests-tab.png?raw=true)
Click on the tab, and on the pull request, and then merge the pull request.
5. Your fork should now be up to date--the status line will confirm this.

## 6. Resources
These Github tutorials might be useful:
- [Github flow](https://guides.github.com/introduction/flow/): describes branch, commit, pull, etc. 5 minute read.
- [Hello world](https://guides.github.com/activities/hello-world/): step-by-step explanation of key functions via web interface. 10 minute read.
- [Understanding Github](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/): very clear introductory discussion, focusing on command line interface.
