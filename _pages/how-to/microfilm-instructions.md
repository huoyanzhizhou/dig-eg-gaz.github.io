---
layout: page
title: Microfilm instructions
permalink: /how-to/microfilm-instructions/
author: Will Hanley
image:
  image_fullwidth: masthead.jpg
---
## The Basics
1. Get film NP 486 for the appropriate month and year from the reserve desk in the basement in Strozier. You can sign it out for two hours.
2. Log on to one of the six microfilm-enabled computers, and open the "Microform PowerScan/PowerScan 1000 or 2200" program. Indicate that you are using microfilm. If you are using PowerScan 2200, please select the "Expert User + New Features" mod so you can change the resolution. Thread the film into the microfilm reader (a "ScanPro 1000/2200"), carefully following the threading route mapped on the table or the machine itself. Run a bit of film through the machine until you begin to see page images--the first foot of film is only black.
3. Familiarize yourself with the controls at the bottom of the program. The "Motorized Roll Film Control" allows you to move through the film and find the issue you need. The toggle switch at the top moves the film slowly, and is useful to make exact adjustments. The larger "Adjust Image" menu has numerous controls. If your image is only displaying as half screen, click the "Film Orientation" button (or "Fill to Width" under the "Home" menu if you are using Powerscan 2200) and it will shift to full screen. You can play with the zoom until you see a whole page on the screen--you may have to move the carriage in the microfilm reader itself to center the image. You can focus, change the brightness, and so on, which will give you a more readable result.
4. When you're happy with what you see, save what's on your screen. Enlarge the green box so that it encompasses the whole area that you want to save. Under the Scan/Print tab, change the scan resolution to 600dpi. Press "Scan to Drive #1." Name your file following the standard dating format plus page number (YYYY-MM-DD-p1). Choose file type jpg.
5. Find the image files you've created on the computer's hard drive, and copy them to a USB key, save them to Dropbox, or save them some other way. Do not simply leave them on the microfilm computer.
6. Return the microfilm to the checkout desk--your classmates will need to find it.

## For Best Results
1. The preceding steps produce a human-readable image, but this image will not be good enough for OCR. In order to produce a high-quality, OCR-ready image, it is necessary to scan the page in quarters, then stitch the image together. Zoom in on the image until the screen shows just the top left-hand quarter of the page, thus:
![quarter page example](https://github.com/dig-eg-gaz/dig-eg-gaz.github.io/blob/master/images/quarter-page-example.jpg?raw=true)
Make sure that you leave a bit of overlap, so that the image stitching software can do its task. Change the shape of the green box, which shows the part of the image that you will save to a file, so that it contains the edges of the print. Now you are ready to save it as an image file. Under the Scan/Print tab, change the scan resolution to 600dpi. Press "Scan to Drive #1." Name your file following the standard dating format plus page number plus a suffix for the top left hand corner (YYYY-MM-DD-p1a). Choose file type jpg. Then proceed to scan the bottom left hand corner (p1b), the top right (p1c), and the bottom right (p1d).
4. Stitch the four quarters into a single high-resolution file using the [Microsoft Image Composite Editor](http://research.microsoft.com/en-us/um/redmond/projects/ice/). The program is loaded on all of the scanning computers at Strozier. If you use a Windows computer, it is free to download for your own computer. When you open the program, click "New Panorama," import the four quarter images you just produced, click "Stitch," then click "Export." Choose image quality "superb," and save the file with the name "YYYY-MM-DD-p1.jpg". This is the file that you will use for subsequent work--save it to your hard drive.
4. Go ahead and do the same for all the pages of the issue. **Note:** You may find that certain pages (often page 1) are doubled on the microfilm. When this is the case, you only need scan one version of the doubled page.
7. Once you are satisfied with your images, upload them directly to the appropriate subfolder within the [page-images repository](https://github.com/dig-eg-gaz/page-images) repository on GitHub. There are four subfolders (one for each quarter of the year). Make doubly sure *before you upload* that your images are named exactly according to this format: `YYYY-MM-DD-p1.jpg` (substitute .png or .pdf if using those format).

### Troubleshooting
Sometimes the microfilm hardware fails to function. When this is the case, follow these instructions (courtesy Malcolm Shackelford of FSU libraries): Those MF machines are prone to fits, but the cure is nearly always to

1. stop the microform viewing/scanning application.
2. turn off the MF machine using the switch on the rear left
3. detach and reattach the firewire cable from both the MF machine and the computer
4. fire up the machine, then the scanning program

Doing the above makes sure we don't have a loose cable, and reminds Windows that the device is there and alive.
