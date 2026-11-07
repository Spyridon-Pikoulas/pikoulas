---
layout: page
title: "How to take a full page screenshot in Chrome"
description: "Chrome can already capture a full page for free. Here are its steps, the free alternatives, and how to crop, mark up and cover details with Marginshot."
permalink: /marginshot/full-page-screenshot-chrome/
theme: extensions
---

# How to take a full page screenshot in Chrome

You do not need an extension to capture a whole page. Chrome has a free command for it, hidden in
its developer tools. An extension or an editor only earns its place if you do this often or want
to mark up the result.

## 1. Use Chrome's own command

1. Open the page and let it finish loading.
2. Press **F12** or **Ctrl+Shift+I** on Windows or Linux, or **Command+Option+I** on a Mac, to open
   DevTools.
3. Press **Ctrl+Shift+P**, or **Command+Shift+P** on a Mac, to open the
   [Command Menu](https://developer.chrome.com/docs/devtools/command-menu).
4. Type `screenshot` and choose **Capture full size screenshot**. Chrome saves the image, normally
   to your Downloads folder.

There is no editor, so crop or mark up the file elsewhere. It does not suit every page either:
[Zapier's test](https://zapier.com/blog/full-page-screenshots-in-chrome/) found it works best on
text-heavy pages and captured only the visible window in Google Docs.

Chrome can also save a page as a PDF. Press **Ctrl+P**, or **Command+P** on a Mac, and choose
**Save as PDF** as the [destination](https://support.google.com/chrome/answer/1069693?hl=en). You
get print pages rather than one long image, so the layout can differ from what you see on screen.

## 2. Check what else is already free

On Windows, the [Snipping Tool](https://support.microsoft.com/en-us/windows/apps/use-snipping-tool-to-capture-screenshots)
opens with **Windows logo key+Shift+S** and can crop, draw and highlight. Its
[Quick redact](https://www.microsoft.com/en-us/windows/learning-center/your-guide-snipping-tool)
hides email addresses and phone numbers. Microsoft lists no scrolling mode, so it captures what
fits on screen.

[Microsoft Edge](https://www.microsoft.com/en-us/edge/features/web-capture) captures long pages
without an extension. Press **Ctrl+Shift+S**, choose **Capture full page**, then draw on the result
before you copy or save it. You would need to open the page in Edge and sign in there if the page
requires it.

You do not need to buy Marginshot to capture a full page.

| Option | Useful for | Check before relying on it |
| --- | --- | --- |
| Chrome's command | A full page with nothing to install | No editor; some web apps capture only the visible window |
| Windows Snipping Tool | Anything on screen, with crop, pen and highlighter | No documented scrolling capture |
| Microsoft Edge | A full page with drawing on top | The page has to be open in Edge |
| [GoFullPage](https://chromewebstore.google.com/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl) | Unlimited full-page captures, exported as PNG, JPEG or PDF | Cropping, text, highlight and blur are in [Premium, $1 a month](https://gofullpage.com/premium) |
| [FireShot](https://chromewebstore.google.com/detail/take-webpage-screenshots/mcbpblocgmgfnpjjppndjkmgjaogfceg) | Whole page, visible part or selection, saved as PDF, PNG or JPEG | Editing and some PDF features are listed under its [paid upgrade](https://getfireshot.com/buy.php) |
| [Scrnli](https://chromewebstore.google.com/detail/screen-recorder-screensho/ijejnggjjphlenbhmjhhgcdpehhacaal) | Full-page and area capture with text, arrows and highlights, plus screen recording and link sharing | We could not confirm its free editor and export limits |
| [Marginshot](/marginshot/) | Full page, visible page or area, then crop, arrows, text, highlights and solid covers, kept on your computer | Ten new edited captures a month for free; no capture of pages that scroll inside a panel |

GoFullPage's listing says it handles inner scrollable elements and embedded frames, which
Marginshot does not. These descriptions come from each publisher's own pages, checked on
6 November 2026. We have not run a head-to-head test, and we do not claim to beat these tools on
every feature. This guide is written by Marginshot's developer.

## 3. Capture the page with Marginshot

1. Install Marginshot from the [Chrome Web Store](https://chromewebstore.google.com/detail/marginshot-screenshot-ann/khiednhplkpcpgmfenmkgggkmhklbkip).
2. Open an ordinary web page and let it settle. Close any cookie banner first: fixed elements stay
   in the first screen of the capture and are hidden after that, so a header appears once rather
   than repeating. If the page loads images as you scroll, scrolling to the bottom and back first
   can help.
3. Click the Marginshot button, in Chrome's Extensions menu if you have not pinned it, and choose
   **Full page**. Use **Visible page** or **Choose an area** for something smaller.
4. Stay on the tab and do not resize or zoom. Marginshot scrolls the page and joins the pieces,
   taking at least half a second per screen height. Press **Esc** or **Cancel** to stop; your
   scroll position is put back either way. The editor opens in a new tab when it finishes.

Marginshot stops with a message rather than saving part of a page. That happens when the page
changes height or navigates during capture, which is common on infinite feeds, and when it scrolls
sideways or inside a panel. Very complex pages and pages beyond 80 screen heights, 30,000 pixels
per side or 64 megapixels also stop it. **Visible page** or **Choose an area** usually gets you the
part you need.

It cannot capture Chrome's own pages, the Web Store, Chrome's PDF viewer or incognito windows.

## 4. Mark it up and save it

Use **Crop**, **Arrow**, **Text**, **Highlight** and **Cover** on the left. **Ctrl+Z** undoes and
**Ctrl+Shift+Z** redoes. Your work saves on your computer as you go, and you can reopen it from
**Saved captures**.

Choose PNG, JPEG or PDF, then choose **Save image** or **Save PDF**. Files go to a `Marginshot`
folder in your downloads. **Copy image** puts a PNG on the clipboard. An export over 32 MB fails
with a suggestion to use JPEG or crop a smaller area. PDF pages are images, so their text cannot be
selected; use Chrome's **Save as PDF** if you need that.

To hide something, use **Cover**, not **Highlight**. A cover is solid and is flattened into exported
images and PDFs, while a highlight is translucent. The covered pixels remain in your editable project,
and **Save original** exports the image without any edits. Check the exported file before you share
it, and use **Delete capture** or **Clear saved captures** to remove projects you no longer want.
Files you already exported stay where you saved them.

## What is free

Original captures and exports are unlimited within your device's storage. A capture with no crop or
marks uses no allowance. Free also includes ten new edited captures per local calendar month. A
capture uses one on its first successful edited copy or export; failed attempts do not spend it.
After that, more edits, other formats and repeat exports of that capture stay free. Deleting a
capture does not give its allowance back. Marginshot Pro removes the limit for **$7.99 once**.

Screenshots and editable projects stay on your computer, with no cloud upload or hosted sharing.
That also means uninstalling Marginshot or losing your browser profile can remove saved projects,
so keep exported copies of anything you want to retain.
[Marginshot's page](/marginshot/) has the terms, refunds and privacy policy.
