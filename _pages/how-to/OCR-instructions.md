---
layout: page
title: OCR instructions
permalink: /how-to/OCR-instructions/
author: Will Hanley
header:
  image_fullwidth: masthead.jpg
---

## Objective
This lesson explains how to turn images of text into editable files. Use this technique to work with free text wherever you encounter it in the *Egyptian Gazette*. Do not use this technique to work with text that has been [templated](https://dig-eg-gaz.github.io/how-to/templating-instructions/). Once you've transformed OCRed text and performed basic corrections, it will be ready for [TEI-XML markup](https://dig-eg-gaz.github.io/how-to/tagging-people-and-places-instructions/).

<div class="panel radius" markdown="1">
**Contents**
{: #toc }
*  TOC
{:toc}
</div>

## 1. Transform image into Text

### If you are using Windows:
1. Download [AABBY Finereader](http://trial.abbyyusa.com/download-fr12pro). The 30-day, 100-page free trial that they offer *should* be enough time to complete your OCR work for this class. If you don't complete it on time, you have the option to buy the software for about $100.
2. Open the program, then open the image file of the page you wish to read. When you open the document, Finereader will automatically read it. Let it do its work.
3. Once the initial read is complete, you'll need to make sure that it's defined the areas correctly. The areas are the green-bordered boxes of text. Often the machine will skip a word, or draw an extra few words in from a different column. You need to have the whole text read in the proper order, so you'll want to reshape these boxes so that they cover the text correctly. I've sometimes found that it's best just to drag one box so that it covers a whole column. You can delete the boxes covering any advertisements or other templated material--you'll copy and paste templates rather than OCR those items.
4. Once the boxes cover all of the text, you need to make sure that they're in the right sequence. Click the tool on the left hand menu with a blue down arrow and a red up arrow. This is the tool to reorder the areas of text.
4. It is possible that your page contains text in French. If this is the case, enclose that text in its own area and set the language (in the "Area Properties" tab at the bottom of the screen) to French.
5. Once the sequence of areas is correct, click the "read" icon again. The program will reread the text in the order you've indicated.
6. Click on the "verification" icon, and proceed to correct the text. When verifying the text, remember that you are only correcting the automatic reading. *Do not* correct any errors you might find in the newspaper itself--not even minor spelling errors. We want to preserve the newspaper in its original text, warts and all.
7. Once you've verified some or all of the text, save your verification work. (If you close Finereader without saving the verification separately, you will lose your work). To do this, use the "Save" icon in the middle top of the page. Choose "Plain text" or "Word Document" as the document layout (as you like), and click "Save." Name the document following the standard format of YYYY-MM-DD-p#. If you click "Format options," and check "Use blank line as paragraph separator," it will make your work easier later on. You can now close Finereader without losing your verification work.
8. Once you've finished work on the page, upload it to your personal GitHub repository.

### If you are using Mac:
This is one of the rare instances when you may be better off using Windows. If you can get ahold of a Windows machine and use Finereader following the instructions above, that may be easier. If not, you can use the Mac version of Finereader, which you can [download here](https://trial.abbyyusa.com/download-frpro-mac-free-trial). The Mac version lacks a verification tool, but it works okay. When you open the .dmg file you've downloaded, don't install the program by dragging it into your applications folder. Instead, doubleclick the Finereader icon and run the program directly. That way you may face fewer problems if your trial period runs out.

To use Finereader on a mac, follow steps 2 to 5 of the instructions above. Then, click "Export." Choose a format (I recommend plain text, but .doc is also useful) and save the file. Then open that file for text correction and to transfer the text into the Oxygen XML editor.

### If your trial license runs out:
The free version of [Finereader Online](finereaderonline.com) allows you to OCR 10 pages per month. This should help if you don't manage to finish all of your OCR in time. Note that there is no verification tool in the online version.

## 2. Move the text into your XML file

Open a the text file that you've corrected, and copy the contents. In the xml file that you're preparing, locate the `<div type="page"> </div>` pair of tags corresponding to the page you're transforming. Paste the text in between these tags. Atom will immediately tell you that you have many errors and issues. Don't fret--we'll address them in the next step. Save the file.

## 3. Add basic structural tags
Wrap the text in tags. For now, we'll limit ourselves to three tags:
-  `<div type="item">`, which you can use for articles, items, or any division of the page that makes sense to you,
- `<head>`, which indicates a headline (the headline must be the first element in the item),
- `<p>`, which indicates a paragraph.

Oxygen offers many shortcuts to make this work go faster. Highlight the text you wish to wrap, then hit `command-E`. You will be offered a menu of tags. Choose the one you want. If you want to add more tags of the same type, hit `command-slash`.

Once you add these tags to your page, you might have a valid document (an thus a green box in Oxygen). But these common errors will probably also have to be addressed:
- **&**: the ampersand is represented as `&amp;` in xml. `&` alone will create an error.
- **>** or **<**: the OCR process produces stray angle brackets. The editor thinks these are part of a xml tag, and it causes an error.
- anything else not in a `<div>`, and not in a `<p>` or a `<head>`.

## 4. Add feature attributes
There are many recurring features that show up issue after issue: local news, international news, sports, and many more. It is important to mark these using the feature attribute, so that we can find them in XPath searches. The complete list of features is [here](https://dig-eg-gaz.github.io/features/). To add an feature attribute, place it within the `<div>` tag, after the `type="item"` attribute.

## 5. Add more complex structural tags
There are more tags that you can add:
- If the article or item is in French, add the attribute `xml:lang="fr"` to the `<div>` tag.
- **`<cb/>`** for column breaks. Be sure to put this tag at the *beginning* of the column. Add the number of the column, as well, thus: `<cb n="1"/>` For mixed columns, see [this guidance](http://dcs.library.virginia.edu/digital-stewardship-services/tei-encoding-guidelines/#cb).
- **`<div type="section">`** to wrap multiple items that belong together, for instance in the international or local news sections.
- **`<dateline>`** for datelines. There can only be one dateline per division. In the international news section, this means that you must make a new `<div type="item">` for each newswire report.
- **`<byline>`** for authors. There can only be one byline per division.
- **`<gap/>`** for holes in the text, **`<unclear>`** for illegible text (you can supply an attribute explaining why), and **`<supplied>`** for something that was illegible but which you figured out by finding the same thing in a different issue.
- pieces of articles that are continuous texts broken up by ads or between issues should be connected using xml:id and the next and prev elements, thus: if the articles are in the same issue, make their tags `<div type="item" xml:id="item1" next="item2">` and `<div type="item" xml:id="item2" prev="item1">`. If the articles are in different issues, make their tags `<div type="item" xml:id="item1" next="YYYY-MM-DD.xml#item2">` and `<div type="item" xml:id="item2" prev="YYYY-MM-DD.xml#item1">`.
- the **`<figure>`** element will be useful for the *Egyptian Gazette*, but I have not yet worked out how to use it.

## 6. Add content tags
This is a more advanced undertaking. See the separate tutorial [here](https://dig-eg-gaz.github.io/how-to/tagging-people-and-places-instructions/).

## FAQs

### How many errors should I expect to find?

If you find a very large number of errors, you might consider re-scanning the page at a higher resolution or a better focus.

### How do I deal with accented letters?

Preserve all accents (e.g. in words like début). You will need to enter accents as single characters. To do so, use the extended keyboard. Here are some pointers for [Windows](https://kb.iu.edu/d/aihp) and [Mac](http://symbolcodes.tlt.psu.edu/accents/codemac.html).

### What if I can't read the text?

Wrap it in an `<unclear>` tag, and maybe add a `<!-- comment -->` explaining what's going on.

### Are there other OCR programs available for Mac?
I've also had good results with [Cisdem OCR Wizard](https://www.cisdem.com/ocr-wizard-mac.html). I'm not sure how long their free trial lasts, but it's worth a try, and can also be purchased for $60. Follow the directions below.

(There are other options, too, but none seems to work as well as Cisdem: you could try the 10-day, 100-page trial of [Readiris Pro](http://www.irislink.com/EN-US/c1195/10-Day-FREE-Trial---Experience-Readiris-Pro-15--OCR-Software-.aspx?utm_source=IRISLINK&utm_medium=Popup&utm_campaign=Popup-trial). [PDF OCR X Community Edition](http://solutions.weblite.ca/pdfocrx/download_mac) also didn't do a great job, but it's free).

#### Using Cisdem
1.  Open the program, then open the image file of the page you scanned (likely page 2 or 3). When you open the document, Cisdem might automatically analyze it, or it might require you to press "recognize". Let it do its work.
3. Cisdem seems to recognize newspaper columns quite well, and you can probably simply proceed to OCR once the recognition is finished and correct by hand later. But if you notice egregious errors, reshape the green boxes.
5. Select .text or .docx as the output format, and click export. Wait. When you are offered the option to save the document, name it following the standard format of YYYY-MM-DD-p#.
6. Once you have saved the text file, open it and proceed to correct the text. It may be most convenient to have the image file on one half of the screen and your text editor on the other. When verifying the text, remember that you are only correcting the automatic reading. *Do not* correct any errors you might find in the newspaper itself--not even minor spelling errors. We want to preserve the newspaper in its original text, warts and all.
8. Once you've finished work on the page, save it--soon we'll upload it to your xml issue file.
