---
layout: page
title: "How to add Google Photos™ to Google Slides™ in bulk"
permalink: /photofill/google-photos-to-google-slides/
description: "Google Slides™ has no button to import an album from Google Photos™. What its own panel does, a free script for a folder of photos, and an add-on that does hundreds at once."
---

# How to add Google Photos™ to Google Slides™ in bulk

A slideshow for a wedding, a memorial, a graduation or a school year usually starts as a few
hundred photos in Google Photos™, and Google Slides™ has no button to import an album. There are
three ways to get them onto slides.

## 1. Slides' own panel (no setup, a few photos)

In the presentation, Insert > Image > Drive & Photos opens a panel on the right. Its Google
Photos™ tab lists your photos by date. Clicking a photo puts it on the slide you are on, sized to
fit the slide.

That is one photo per click, all on the current slide. For a photo per slide, add a slide (Ctrl+M)
before each click. It works for ten photos, but it is slow for three hundred.

## 2. Download them, then a script (free, some setup)

1. In Google Photos™, open the album, then its menu (⋮) > Download all. You get a zip file.
2. Unzip it and upload the folder to Google Drive™.
3. In the presentation, go to Extensions > Apps Script and replace everything in `Code.gs` with
   the code below.
4. Put your folder's ID in place of `FOLDER_ID`. The ID is the last part of the folder's URL in
   Drive.
5. Click Run, and allow the access it asks for: it reads your Drive to find the folder.

```js
function imagesToSlides() {
  var folder = DriveApp.getFolderById('FOLDER_ID');
  var deck = SlidesApp.getActivePresentation();
  var files = [];
  var it = folder.getFiles();
  while (it.hasNext()) {
    var f = it.next();
    if (/^image\/(png|jpeg|gif)$/.test(f.getMimeType())) files.push(f);
  }
  files.sort(function (a, b) { return a.getName().localeCompare(b.getName(), undefined, { numeric: true }); });
  var W = deck.getPageWidth(), H = deck.getPageHeight();
  files.forEach(function (f) {
    var img = deck.appendSlide(SlidesApp.PredefinedLayout.BLANK).insertImage(f.getBlob());
    var k = Math.min(W / img.getWidth(), H / img.getHeight());
    img.setWidth(img.getWidth() * k).setHeight(img.getHeight() * k);
    img.setLeft((W - img.getWidth()) / 2).setTop((H - img.getHeight()) / 2);
  });
}
```

It adds one slide per image at the end of the presentation, with each image scaled to fit and
centered. The slides follow the file names, with numbers in numeric order, so IMG_9 comes before
IMG_10. That is not always the order the photos were taken in.

Slides takes only PNG, JPEG and GIF images up to 50 MB and 25 megapixels:

- The script skips iPhone HEIC photos, so convert them to JPEG first.
- A larger image stops the script with an error, so shrink it first.

Apps Script also stops any run after 6 minutes. For a very large folder, split it into a few
smaller ones.

## 3. PhotoFill (free for 30 photos a day)

I built [PhotoFill](/photofill/) for this, so no download and no Drive copy are needed. In the
presentation:

1. Go to Extensions > PhotoFill > Open PhotoFill.
2. Click "Pick photos from Google Photos". Google's own picker opens in a tab, where you select
   your photos and click Done.
3. Choose a layout, an order, a caption and a background, then click "Add to slides".

You can select up to 2,000 photos in one pick. Google lets add-ons take only the photos you
select, not a whole album in one click. In an album, click the first photo's check mark, then
Shift-click the last one to select everything in between.

The options are:

- **Layout**: one photo a slide (the whole photo, or filling the slide with the edges cropped),
  or two or four a slide.
- **Order**: as picked, by date taken (oldest first), or by file name.
- **Caption**: the date taken, the file name, or none.
- **Background**: your theme's, black or white.

New slides go after the one you are on, so you can start with a title slide. Each photo goes in at
its own size, up to 4K, which is 3840 pixels on its long side and the most Google Slides™ keeps.
Tick "Lighter file" for photos at most 2560 pixels across when the presentation has to stay small.

Big picks go in rounds, with a progress line and a Stop button. A photo that can't be added is
named, not silently dropped, and videos are skipped and counted.

PhotoFill reaches only the photos you pick and the presentation you open it in. It is free for 30
photos a day. PhotoFill Pro has no limit and costs $5.99 a month, $29 a year, or $4.99 for a
7-day pass that doesn't renew.

[Install PhotoFill from the Google Workspace™ Marketplace](https://workspace.google.com/marketplace/app/photofill_insert_import_photos_images_in/714992365817)
