---
layout: page
title: "How to redact a screenshot before you share it"
description: "Blur and translucent highlights can leave private details readable. Use a solid cover, share a flattened copy and check it. Free tools first, then Marginshot."
permalink: /marginshot/redact-a-screenshot/
theme: extensions
---

# How to redact a screenshot before you share it

Redacting a screenshot means removing the pixels that show an email address, a name or a number,
not just making them harder to read. Three rules hold whichever tool you use:

1. **Cover the detail with a solid, fully opaque box**, with some margin around it. Blur,
   pixelation and see-through highlights leave information behind.
2. **Share a newly saved, flattened copy.** An editable file can still hold what is under the box.
   Save the result as a new file rather than over the original.
3. **Open the copy you are about to send and check it.** The same detail often appears more than
   once: in a greeting, an account menu, a page header, a reference number or a QR code.

## Cover, blur and highlight are not the same

- **Solid cover:** every pixel inside the box becomes one color. Once the image is flattened,
  nothing of the original remains there.
- **Blur and pixelation:** each new pixel is still an average of the pixels underneath. When the
  text is in a known font, it can be guessed back; Bishop Fox's
  [Unredacter](https://bishopfox.com/blog/unredacter-tool-never-pixelation) recovered pixelated
  text this way. Do not rely on it for an email address, an account number or a password.
- **Translucent highlight:** the original shows through, because a highlight exists to draw
  attention to text, not to hide it.
- **A box drawn over a picture in an editable document,** such as a shape in Word or PowerPoint
  or an annotation in a PDF, sits on top of the original. Anyone with the file can move or delete
  it. Export a flattened image instead.

## 1. Leave it out before you capture

On a web page, the safest detail is one that never reaches the image. Capture only the area you
need, or replace the text in Chrome first:

1. Right-click the email address or name and choose **Inspect**.
2. In the **Elements** panel, double-click the highlighted text and
   [type a placeholder](https://developer.chrome.com/docs/devtools/dom#edit), such as
   `name@example.com`. Press **Enter**.
3. Take the screenshot. Only your copy of the page has changed, and reloading it brings the real
   text back.

This works for text on the page. Text inside pictures, videos and form fields you have typed into
needs covering instead.

## 2. Free tools that cover details

You do not need to buy Marginshot to redact a screenshot.

| Option | How it hides details | Check before relying on it |
| --- | --- | --- |
| [Windows Snipping Tool](https://www.microsoft.com/en-us/windows/learning-center/your-guide-snipping-tool) | **Windows logo key+Shift+S**, open the snip, choose **Text actions**. **Quick redact** hides email addresses and phone numbers; select other text and right-click to redact it | It finds only what its text recognition reads; names, addresses and account numbers need selecting by hand |
| [Mac Markup](https://support.apple.com/guide/mac-help/mchl1fd88863/mac) | **Shift-Command-4**, click the thumbnail, add a rectangle from **Shapes** and set its **Fill Color** | An unfilled rectangle is only an outline |
| [Greenshot](https://getgreenshot.org/help/) | Free, open-source Windows editor with rectangles that take a fill color | Its obfuscate tool pixelates or blurs; use a filled rectangle for text |
| [Full Page Screen Capture](https://chromewebstore.google.com/detail/full-page-screen-capture/pmabjgjpcbofkbbeiphkiaanogobokgg) | Chrome extension with solid redaction boxes, blur, pixelation and one-click detection of personal information | Its listing says it is free with no paid tier; choose the solid box, not blur |
| [Private Screenshot Redactor](https://chromewebstore.google.com/detail/private-screenshot-redact/piaajlkipcdmcdkdffecmcphcfljkbck) | Chrome extension that paints black boxes into the saved PNG; manual boxes are free | Visible part of the tab only; suggested boxes from local text recognition are $3.99 once |
| [Marginshot](/marginshot/) | Solid covers flattened into PNG, JPEG and PDF exports, plus crop, arrows and text | No automatic detection; ten new edited captures a month for free |

Automatic detection helps, but none of these tools promises to find everything, so look over the
result yourself. Microsoft fixed a
[Snipping Tool flaw](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-28303) in 2023
that could leave cropped-out parts recoverable when an edited image was saved over the original
file. Keep your tools updated.

The descriptions of other tools come from their publishers' pages, checked on 7 November 2026. We
have not tested them. This guide is written by Marginshot's developer.

## 3. Cover details with Marginshot

1. Install Marginshot from the [Chrome Web Store](https://chromewebstore.google.com/detail/marginshot-screenshot-ann/khiednhplkpcpgmfenmkgggkmhklbkip).
2. Click the Marginshot button and choose **Visible page**, **Choose an area** or **Full page**.
   The image holds the page itself, not Chrome's address bar, tabs or other windows. Choosing an
   area that leaves the private part out is the surest redaction of all.
3. In the editor, choose **Cover** and drag over each detail. A cover is a fully opaque box in the
   **Color** you pick. **Crop** removes everything outside the crop from exports.
4. Look over the whole image, zooming in with **+** on long captures. Marginshot does not detect
   private details for you; it has no text recognition.
5. Choose **Save image** for PNG or JPEG, **Save PDF**, or **Copy image**. Every one is newly made
   from the flattened picture. A PDF holds only images of that final picture, with no text layer
   and no original image. Open the file and check it before you send it.

Do not use **Highlight** to hide anything: Marginshot paints highlights at 30% opacity, so the text
underneath stays readable. **Save original** exports the capture without any edits, covers
included, and its file name ends in "original".

The exported file is named after the capture. Its default name is the date and time; if you rename
it, keep the private detail out of the name.

## What Marginshot keeps on your computer

The editable project keeps the original capture, including the pixels under your covers. A cover
stays a mark you can select, move or delete, which lets you fix a mistake. It also means anyone
using your browser profile could open **Saved captures** and remove it.

Saved captures have no automatic expiry. Once you have shared the export, choose **Delete capture**
in the editor, or **Clear saved captures** in **Settings**, to remove the editable original. Files
you exported stay where you saved them. Screenshots, projects and their names are never uploaded.

## What is free

A covered screenshot counts as an edited capture. Free includes ten new edited captures per local
calendar month. A capture uses one on its first successful edited copy or export; failed attempts
do not spend it. After that, more edits, other formats and repeat exports of that capture stay
free. Deleting a capture does not give its allowance back. Marginshot Pro removes the limit for
**$7.99 once**. [Marginshot's page](/marginshot/) has the terms, refunds and privacy policy.
