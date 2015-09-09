---
author: archiver
comments: true
date: 2003-05-07 22:56:49+00:00
excerpt: None
layout: post
slug: neat-tricks
title: Neat Trick(s)
wordpress_id: 1574
tags:
- oldpost
---

To combine multiple postscript files into one PDF or PS file:<blockquote>gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=out.pdf -dBATCH file1.ps file2.ps ...<br /><br />gs -dNOPAUSE -sDEVICE=pswrite -sOUTPUTFILE=out.ps -dBATCH file1.ps file2.ps ...</blockquote>To shrink multiple pages from one postscript file onto one page:<blockquote>psnup -N file.ps > out.ps</blockquote>Where N is 2, 4, 6, 8, etc. (not sure how high it can go).<br /><br />-Oliver