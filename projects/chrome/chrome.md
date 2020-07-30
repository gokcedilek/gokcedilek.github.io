---
layout: post
title: Chrome Extensions!
# subtitle: Each post also has a subtitle
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
tags: [chrome][javascript]
comments: true
---

Timeline: Jun 2020

Here are some quick & easy (not so easy while working on it:) Google Chrome extensions I worked on - I wanted to explore developing extensions due to several reasons:

- My general interest towards web development
- My curiosity about how easy/hard it would be to get started with developing extensions
- The thought/potential of building cool little helpers for your browsing experience

**Project #1:** _Copy/Paste Stack_
This extension implements a copy/paste stack for users such that successive text they _copy_ (with cmd/ctrl + c) is saved to a stack, and is removed from the stack as they _paste_ (with cmd/ctrl + p). The extension works across multiple tabs and multiple windows.

Challenges faced/Things learned:

- working with the Chrome API, content scripts, background scripts, and message-passing between the content & background scripts
- using custom data types and ES6 modules in the extension
- using the asynchronous [Clipboard API](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API)

**Project #2:** _Read Later_ (Incomplete, ongoing!)
This extension (is expected to implement:) implements a special bookmarks folder in Chrome to which the user can add webpages to review later, and the extension recommends one page to read from this folder everytime the user opens the Google home page.

What has been implemented so far:

- Adding the special bookmarks folder to user's browser upon installing the extension, adding pages to the folder, retrieving the list of pages when the Google home page is visited.
