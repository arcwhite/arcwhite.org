---
author: admin
comments: true
date: 2010-02-03 18:40:53+00:00
layout: post
slug: google-custom-search-refinements-and-the-csbe-api
title: Google Custom Search Refinements and the CSBE API
wordpress_id: 261
categories:
- IT
tags:
- api
- google
- labels
- query strings
- refinements
- search
---

As part of my duties at [SitePoint](http://sitepoint.com), I'm implementing a Google Custom Search Engine (Business Edition).

One of the neat features of Google's CSE is Refinements. You can tag portions of your site - subdirectories, subdomains, or even separate sites that you've added to your engine - with labels. You can then create refinements that will either boost results from these tagged regions of your site, list only results from specified tags, or exclude certain tags altogether from the result set.

Unfortunately the means of using these programmatically are not so well documented - the API documentation doesn't specify how to include or exclude certain labels (as far as I've been able to determine).

So! For the record, the solution is to use the strings '**more:<label>**' and '**less:<label>**' in your query string.

<!-- more -->

If you have a refinement called 'Forums', for example, and you've set your custom search engine to 'search only labeled sites', entering a query like '**toast more:forums**' will show results only from your Forums refinement. Similarly, the query string 'toast less:forums' will remove results from the result set that would have been taken from sites you've labelled 'Forums'.

You can also combine refinement labels - if you have labels 'Forum', 'Blogs' and 'Articles', and you want to exclude forums and blogs, you could construct a search like '**winnebago less:forum less:blogs**', and this will only show your article results.

The more you know!
