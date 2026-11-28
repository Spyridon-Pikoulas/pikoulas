---
layout: page
title: "How to see YouTube timestamp comments at their moment"
description: "Comments like \"2:41 the drop!\" are buried in a long list. How to find them on YouTube itself, the free extensions that mark them on the timeline, and Crowdtime, which plays them as a live chat."
permalink: /ytchat/youtube-timestamp-comments/
theme: extensions
---

# How to see YouTube timestamp comments at their moment

A timestamp comment names a moment of the video: "2:41 the drop!", "12:05 he actually did it". They
are often the best comments, and the hardest to find: YouTube lists them among every other comment,
and the one about 2:41 is only worth reading at 2:41.

## 1. On YouTube itself

YouTube turns a time in a comment into a link. Click **2:41** in a comment and the video jumps
there; this works in replies too, and in the phone app.

YouTube has no filter for them, but you can narrow the list:

1. Under the video, open the comments and keep **Top comments** as the order. Timestamp comments
   that people liked come first.
2. Scroll down a few times so more comments load, then press **Ctrl+F** (**Command+F** on a Mac)
   and search for a colon, `:`, or for the minute you want, like `2:4`. The browser finds only
   comments already loaded.

Where it falls short: you find the comment before or after the moment, never at it, and long videos
have thousands of comments to load.

## 2. Free extensions that mark them on the timeline

| Option | What it does | Check before relying on it |
| --- | --- | --- |
| [YouTube Timestamps](https://chromewebstore.google.com/detail/fjchmkcdmgeimkholkgodkejnikeklmh) | Marks timestamps from comments on the video's timeline; hover one to preview its comment. Open source | Its listing says it reads only the first 100 comments |
| [YouTube Timestamp Comments](https://chromewebstore.google.com/detail/khngjoedfeicfbjlcfmiigbokbnlibei) | Lists timestamp comments sorted by time; click one to jump there | A list beside the video rather than at the moment |
| [Timestamped YouTube Comments](https://chromewebstore.google.com/detail/gnpppldhfbbagiaalkddddajadhlgofm) | "See timestamped comments as you watch" | Its listing gives no further detail |
| [TimeComments](https://chromewebstore.google.com/detail/djcmgmddnajefejhjhfhlfljoofplmlo) | Markers above the timeline for each timestamped comment, discussion spikes, bookmarks | AI analysis and loading all comments are Pro |
| [Crowdtime](/ytchat/) | Plays timestamp comments as a live chat when the video reaches them, and marks where they cluster above the progress bar | Reads a video's top 500 comment threads; videos with comments off have no chat |

Descriptions come from each publisher's store listing, checked on 27 November 2026. We have not
tested them. This guide is written by Crowdtime's developer.

## 3. Watch them arrive with Crowdtime

Crowdtime reads a video's comments and replies, picks out every timestamp, and shows each comment in
a chat beside the video when playback reaches its moment.

1. Install Crowdtime from the [Chrome Web Store](https://chromewebstore.google.com/detail/crowdtime-youtube-comment/pocfkgkplocdholjidaikoodpgpincbf).
   It is free, with no account.
2. Open a video and choose **Open chat** in the Crowdtime panel beside it. The panel's footer shows
   how many comments it read and how many carry a timestamp.
3. Play the video. Each timestamp comment appears at its moment; one that lists several moments
   plays line by line. It pauses with the video and follows its speed.
4. To jump, click a timestamp in the chat, or a bar in the strip above the progress bar, where the
   taller bars are the moments people talk about most. Jump anywhere and every timestamp comment up
   to that moment is in the chat at once.

Other top comments drift by in between, marked with a star, and new comments arrive as they are
posted. To see only timestamp comments, open the gear in the panel and switch off **Other top
comments too** and **New comments as they're posted**.

The comments are read from YouTube in your own tab; nothing goes to a server of ours.
[Crowdtime's page](/ytchat/) has the terms and privacy policy.
