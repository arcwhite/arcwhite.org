---
author: admin
comments: true
date: 2009-03-17 13:26:59+00:00
excerpt: 'A project I''m working on had things that needed to be printed. Initially,
  I used FPDF to generate and output a PDF document, which was reasonably pretty and
  very printable.


  Somewhere along the way, I lost my mind and re-implemented these as HTML documents.
  I don''t know what came over me. There was a reason for it at the time. HTML documents
  are a pain in the backside to print, most of the time - browsers usually feel obligated
  to stick headers and footers on them with URLs and dates, and in Firefox at least,
  these are a pain to turn off.'
layout: post
slug: an-ode-to-revision-control
title: An Ode to Revision Control
wordpress_id: 80
categories:
- IT
tags:
- rcs
- software development
- subversion
---

A project I'm working on had things that needed to be printed. Initially, I used [FPDF](http://fpdf.org) to generate and output a PDF document, which was reasonably pretty and very printable.

Somewhere along the way, I lost my mind and re-implemented these as HTML documents. I don't know what came over me. There was a reason for it at the time. HTML documents are a pain in the backside to print, most of the time - browsers usually feel obligated to stick headers and footers on them with URLs and dates, and in Firefox at least, these are a pain to turn off.

So, the call was made to turn them back to PDFs. For most of them this wasn't too hard, or they hadn't been implemented in the first place and needed to be created from scratch in FPDF. One of them was a bit ornate, and had been a PDF before - what a pain, to have wasted all that effort!

Oh-hoh! But I use subversion. My effort was not wasted. Revert to revision 190, code recovered. Bam! I love you, Subversion.

If you're the technological software developer type, you might be wondering now why I'm not using git or bazaar or the like - one of the new distributed RCS tools. Quite honestly, they're overkill for me - I have at most 2-3 other people working on my projects, they're not open source projects that the world will see, so there's really no point to setting up a new RCS when Subversion does the trick.

The rest of you are already smiling and nodding at the crazy computer-man. :D
