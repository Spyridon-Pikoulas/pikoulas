---
layout: page
title: "How to export YouTube comments to Excel or CSV"
description: "YouTube has no button to download a video's comments. Four ways that work, with every reply included, and what each one leaves out."
permalink: /sift/export-youtube-comments-to-excel/
---

# How to export YouTube comments to Excel or CSV

YouTube has no button that downloads a video's comments, not even for the channel that owns the
video. YouTube Studio lets a creator read, filter and reply to comments, but not export them, and
Google Takeout only gives you the comments you wrote yourself. Copying from the page doesn't work
well either: YouTube loads comments in batches as you scroll, keeps replies folded until you open
each thread, and a paste brings the page layout with it.

So every way to get the comments into a spreadsheet reads them from YouTube for you. Here are four,
from the least setup to the most, and what each one leaves out.

## 1. A browser extension: Sift

[Sift](/sift/) is the Chrome extension I make for this. Install it from the
[Chrome Web Store](https://chromewebstore.google.com/detail/sift-youtube-comment-sear/heihjpfnmjbjkbehpogkcigffheppdlj),
open the video on youtube.com, and a Sift bar appears above the comments:

1. Leave **Newest first (all)** selected to load every comment (or pick **Top comments**), and
   leave **Replies** ticked to load every reply as well.
2. Click **Load comments**. The count goes up as they arrive; **Stop** keeps what has loaded.
3. If you only want some of them, narrow the list: a search word, an author, a minimum number of
   likes, comments or replies only, or only comments with timestamps, links or questions (more in
   [How to search YouTube comments](/sift/search-youtube-comments/)).
4. Choose **CSV** and click **Export matches**.

The file opens in Excel or Google Sheets with emoji and every alphabet intact. Each row is one
comment or reply, with its id, the comment it replies to, author, text, likes, number of replies,
when it was posted (as YouTube words it, "3 weeks ago"), whether it's by the creator, hearted or
pinned, and a link to the comment. JSON and plain text are there too.

Exporting up to 500 comments at a time is free; Sift Pro ($7.99, paid once) exports any number.
Sift needs no account or API key and talks only to YouTube. For a Short, open it as a normal video
first: change `/shorts/` in the address to `/watch?v=`.

## 2. A free command-line tool: youtube-comment-downloader

If you have Python and don't mind a terminal,
[youtube-comment-downloader](https://github.com/egbertbouman/youtube-comment-downloader) is a free,
open-source tool that reads comments the way the YouTube page does, also without an API key:

```
pip install youtube-comment-downloader
python -m youtube_comment_downloader --url "https://www.youtube.com/watch?v=VIDEO_ID" --output comments.csv --format csv --language en
```

It saves every comment and reply, newest first; add `--sort 0` for top comments first, or
`--limit 1000` to stop early. `--format scsv` writes semicolons instead of commas, for Excel set to
a European locale. Two things to know before you analyse the file: likes come as YouTube shows
them ("4.8M", "38K") rather than as numbers, and dates are relative ("6 years ago"), with an
estimated Unix timestamp in the `time_parsed` column. Without `--language en`, both come in the
language YouTube picks for your location.

## 3. The YouTube Data API

YouTube's official API is the way to go for exact numbers or a recurring job. It needs a free API
key from a Google Cloud project. Its
[commentThreads.list](https://developers.google.com/youtube/v3/docs/commentThreads/list) method
returns a video's comments 100 at a time, each call costing 1 unit of the default 10,000-unit daily
quota, with exact like counts and exact publication times. Its one catch: each thread comes with
only a few of its replies, and the rest take a
[comments.list](https://developers.google.com/youtube/v3/docs/comments/list) call per thread. If
you'd rather stay in Excel, Chandoo's
[Power Query template](https://chandoo.org/wp/export-youtube-comments-template/) calls the API from
a workbook.

## 4. Web tools

Sites such as [CommentShark](https://www.commentshark.com/youtube-comment-exporter) and
[ExportComments](https://exportcomments.com/) take a video link and hand back a spreadsheet, with
nothing to install. Their free tiers are capped: CommentShark exports the 1,000 most recent
comments without an account and 5,000 with a free login, with the first five replies of each
thread; ExportComments' free plan has a limit that paid plans raise. For a one-off on a smaller
video they're the quickest.

## Opening the file in Excel

- If accents or emoji come out garbled, the file has no UTF-8 marker. Import it instead of opening
  it: Data > From Text/CSV, File origin "65001: Unicode (UTF-8)". Sift's files and
  youtube-comment-downloader's carry the marker and open with a double-click.
- If everything lands in one column, Excel expects semicolons. Use the same import and set the
  delimiter to Comma.
- A comment with line breaks stays in one cell; turn on Wrap Text to read it.
