---
layout: post
title: Blog View Count
key: 20180328
tags: other
---

This is a sad story.

<!--more-->

Though I could receive data from visitng my articles and found them on LeanCloud, the view count is not updated. I found there were javascript codes inserted in _layouts/home.html and _layouts/post.html, but even uncommenting them didn't make a difference. A way to manipulate view count is in _includes/components/article-data.html - simply make the 0 to any other number. This change applies to all articles of course. I double-checked the developer's git page but found identical code. So it is not the fault of code? What is the problem then?