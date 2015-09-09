---
author: Oliver
comments: true
date: 2006-02-05 09:14:39+00:00
excerpt: None
layout: post
slug: hotlinking
title: Hotlinking
wordpress_id: 192
tags:
- misc
---

So I finally looked at my server logs and it seems like I've got a decent number of people hotlinking my images.  Apparently I show up quite high on some Google image searches.  I've decided to put an end to that and modified my htaccess file to block requests for images other than those from oliverweb.com.  *shrug*

Here's a graph of how many requests I got for an image of Pikachu:

<img alt="req.png" src="http://www.oliverweb.com/images06/blog/req.png" width="423" height="249" />

I thought about instead of forbidding access to the picture to replace it with... hmmm... wait, that's actually a good idea... I'll get back to you on that. =)

Edit: OMG, this is hilarious!! Go <a href="http://profile.myspace.com/index.cfm?fuseaction=user.viewprofile&amp;friendID=5126424">here</a> and scroll down a bit... you'll know when you see it. =) (You may need to refresh/reload the page once)... some <a href="http://www.xanga.com/batmanflat/418397592/item.html">more</a>.  Oh... if your firewall is configured to block the HTTP_REFERRER in your browser, it prob won't work and you'll just see sad Pikachu... gotta figure out a way around that...