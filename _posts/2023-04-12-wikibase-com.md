---
layout: post
title: Structured Data in Commons and wikibase software tools
description: I recently wrote a blog post describing how I created Structured Data on Commons, SDoC, depicts statements using spreadsheet data and the VanderBot Python script. The post also describes issues with the Wikimedia Commons Query Service and links to Python code for downloading SDoC data using it.
date: 2023-04-13 17:00:00
hero_image: /img/components_diagram.png
image: /img/madonna_child_diagram.png
hero_height: is-large
hero_darken: true
---

In February, I gave a presentation at the Wikibase Working Hour about how my VanderBot tool for uploading data to Wikidata could be used more broadly with any kind of wikibase. One example I gave was using it to upload Structured Data on Commons (SDoC) statements that describe what is depicted in a media file, since SDoC is just another wikibase instance. 

I recently created a [blog post](https://baskauf.blogspot.com/2023/04/structured-data-in-commons-and-wikibase.html) that briefly describes the issues related to using VanderBot in this way and the steps necessary to do an upload to SDoC. SDoC plays a crucial role in making media items in Wikimedia Commons more discoverable since it helps potential users search based on what the media item depicts. SDoC "depicts" statements can be made manually, but that's very labor intensive. So there is a lot of interest in developing tools that could make the process faster and easier. 

The Wikimedia Commons Query Service (WCQS, an analog of the popular Wikidata Query Service) leverages the fact that wikibase content can be queried using the SPARQL query language. However, the WCQS is more difficult to use programmatically because it requires authentication to access it via HTTP. The [blog post](https://baskauf.blogspot.com/2023/04/structured-data-in-commons-and-wikibase.html) also describes some code that I wrote to make it easy to download SDoC data via the WCQS using Python. This is a key piece for projects to add "depicts" statements since it allows one to determine what depicts statements have already been made about a media file, and avoid creating duplicate statements.



