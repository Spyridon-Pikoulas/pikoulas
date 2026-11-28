---
layout: page
title: "Import Google Drive™ images into Google Slides™"
permalink: /photofill/google-drive-images-to-slides/
description: "Choose private Drive JPEG/PNG files, preview their order and layout, then add them to new slides. Includes Google's free image-insertion option."
---

# Import Google Drive™ images into Google Slides™

For a few pictures, use Google Slides' free image-insertion tools:

1. Open your presentation and select the slide where the image should go.
2. Choose **Insert > Image > Drive & Photos**, then find your image in Drive.
3. Select it and click **Insert** or **Open**. Arrange it on the slide; add more slides as needed.

[Google's instructions](https://support.google.com/docs/answer/97447?hl=en) describe this native
route. You may not need an add-on for a small selection.

For an ordered batch on new slides, [PhotoFill](/photofill/) lets you pick private Drive images,
preview their layout and import them together. I make PhotoFill. Its Drive workflow has been
checked with private JPEGs, including a rotated portrait, and the inserted images were checked
again after closing and reopening the presentation.

## Select files and preview the slides

1. Install PhotoFill from its [product page](/photofill/), open the presentation and choose
   **Extensions > PhotoFill > Open PhotoFill**. Check the account shown in the sidebar.
2. Click **Google Drive**. In Google's file-selection dialog, find and select the JPEG/PNG files
   you want, then click **Select**. Choose the image files themselves: PhotoFill does not import
   or monitor an entire folder automatically.
3. Check the selected names and any unsupported-file notices. Set **Order** to **File name**, or
   use **As selected / manual order** and the earlier/later arrows to arrange the selection.
4. Choose **One per slide, whole image** to keep each photo's edges, or another layout if you
   prefer a crop or several images per slide. Check the preview before importing. Selecting and
   previewing do not add slides or use your free-image allowance.
5. Check the full selection and allowance, then click **Import selection as** followed by your
   account. Wait for completion and inspect the new slides, which go after the current slide.
   Preview thumbnails have less detail than the inserted images.

For date ordering or captions, PhotoFill uses Drive’s image time when present; otherwise it uses
the file’s last-modified time. That fallback is not necessarily when the photo was taken. Use
manual or **File name** order when those dates do not match the chronology you want.

## File limits, access and recovery

Use **JPEG or PNG**, at most **20 MB and 25 megapixels per Drive image**, with up to **500 images
per job**. Convert unsupported formats such as HEIC first. Drive images are resized in your
browser to a maximum 3840-pixel long side; **Lighter file** lowers that to 2560 pixels.

The source files can stay private. You explicitly choose files through Google's picker; this
uses [per-file access](https://developers.google.com/workspace/drive/api/guides/api-specific-auth),
not access to your whole Drive. Imported images become part of your presentation, so consider
who can view that presentation. See PhotoFill's [privacy policy](/privacy/photofill/) for saved
job metadata and processing details.

Use a window signed into only the intended Google account if the sidebar shows another account.
A presentation's account number in its URL does not reliably identify the account used by an
Apps Script add-on. The [account troubleshooting guide](/google-workspace-add-on-wrong-account/)
explains how to switch safely.

You can **Stop after this batch** and reopen PhotoFill in the **same presentation** to continue
its saved job for seven days. Keep access to the original Drive files. If a reply is lost, check
the saved import before starting another one; completed images are preserved. An unrecognized
partial object may need the manual cleanup described in the sidebar before recovery can continue.

New users get **12 successful image insertions free in total**; existing users retain **30/day**.
A **$4.99 seven-day Pro pass** is one payment with no renewal. The whole selection must fit your
remaining allowance before starting: choose fewer images or get Pro. See [current plans](/photofill/#plans).
Google service limits still apply to Pro; check the finished deck before presenting.

For files on your computer, use the [local-image guide](/photofill/upload-multiple-images-google-slides/).
Its [two-image starter ZIP](/media/photofill-example.zip) is a small local-files practice; no Drive upload is needed.
For Google Photos™, use its [separate selection workflow](/photofill/google-photos-to-google-slides/).

Google Drive™, Google Slides™ and Google Photos™ are trademarks of Google LLC. PhotoFill is
independent and is not endorsed by Google.
