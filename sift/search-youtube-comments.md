---
layout: page
title: "How to search YouTube comments by word or user"
description: "YouTube has no search box for a video's comments. What works for any video, for your own channel, and for the comments you wrote yourself."
permalink: /sift/search-youtube-comments/
---

# How to search YouTube comments by word or user

YouTube has no search box for a video's comments. What works depends on whose comments you're
looking for: anyone's on any video, the ones on your own channel, or the ones you wrote yourself.

## On any video

### 1. Ctrl+F, after loading them all

The browser's find (Ctrl+F, or Cmd+F on a Mac) only searches what's on the page, and YouTube adds
comments in batches as you scroll, with replies folded until you click "replies" under each one.
On a video with a few hundred comments, that's workable: choose Sort by > Newest first, scroll until
no more load, then search. Replies you haven't opened aren't searched, and on a video with
thousands of comments the page slows down long before the end. The YouTube app has no find at all.

### 2. Sift: a search box over every comment and reply

[Sift](/sift/) is the Chrome extension I make for this. Install it from the
[Chrome Web Store](https://chromewebstore.google.com/detail/sift-youtube-comment-sear/heihjpfnmjbjkbehpogkcigffheppdlj),
and a Sift bar appears above the comments of any video on youtube.com:

1. Click **Load comments**. It loads every comment and, with **Replies** ticked, every reply.
2. Type in the search box. Every word you type has to be in the comment, in any order, ignoring
   case, and the matches are highlighted. Tick **.\*** to search with a regular expression instead,
   for example `colou?r` for both spellings.
3. To find someone's comments, type part of their name or @handle in **Author**. Other filters:
   minimum likes, comments or replies only, and only comments with timestamps, links or questions,
   or by the creator, hearted or pinned. Sort by most liked or most replied.
4. Click **Open** on a comment to see it in its thread on YouTube, or a timestamp in it to jump the
   video there.

Searching and filtering are free, and so is exporting what you found, up to 500 comments at a
time, to CSV for Excel, JSON or text. Sift Pro ($7.99, paid once) exports any number. The other
ways to get comments into a spreadsheet are in
[How to export YouTube comments to Excel or CSV](/sift/export-youtube-comments-to-excel/).

### 3. A web tool, also on a phone

Extensions don't run in the YouTube app or in most mobile browsers. On a phone,
[Hadzy](https://hadzy.com/) does the same from a website: paste the video's link, let it load the
comments, and search them by keyword or author, with filters for date and likes. It's free and
needs no account.

## On your own channel: YouTube Studio

In [YouTube Studio](https://studio.youtube.com/), open Comments and type in the filter bar's search.
It finds keywords across all the comments on your videos, and, for the last 90 days, comments
about a topic too ("questions about my microphone"). It can't search by user. For that, and for
comments on other channels' videos, use one of the ways above.

## Comments you wrote yourself

YouTube keeps them at
[youtube.com/feed/history/comment_history](https://www.youtube.com/feed/history/comment_history),
signed in with the account you commented from. Every public comment you've posted is listed there
with a link to where you posted it, and Ctrl+F searches the ones loaded so far. Comments on videos
that have since been deleted, or that YouTube removed, don't appear.
