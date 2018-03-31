---
layout: post
title: Blog View Count
key: 20180328
tags: other
---

This is a sad story.

<!--more-->

Though I could receive data from visitng my articles and found them on LeanCloud, the view count was not updated. I found there were javascript codes inserted in _layouts/home.html and _layouts/post.html, but even uncommenting them didn't make a difference. A way to manipulate view count is in _includes/components/article-data.html - simply make the 0 to any other number. This change applies to all articles of course. I double-checked the developer's git page but found identical code. So it is not the fault of code? What is the problem then?

Thanks to Qi this desperation was terminated. Changing the authorization control of my blog_counter class created in LeadCloud solved the problem. First, manually make ACL(Access Control List) for each existing object (i.e. blog post) which has 0 views to `"write":true` for all users. Then existing posts can increment views based on visitor clicks. (Not granting read access for all users doesn't seem to be a problem for view count. Though manipulating these two parameters may create multipe object for the same post which makes it hard to maintain a unique real view count.) Second, grant write access for all users under ACL column setting: `{"_owner":{"read":true,"write":true},"*":{"read":true,"write":true}}`. Then new created posts will be able to count views! Yay!!!

> A happy ending.