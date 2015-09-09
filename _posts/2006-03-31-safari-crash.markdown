---
author: Oliver
comments: true
date: 2006-03-31 07:12:18+00:00
excerpt: None
layout: post
slug: safari-crash
title: Safari Crash
wordpress_id: 208
tags:
- misc
---

Never-mind <a href="http://www.macnn.com/articles/06/03/29/new.flaw.crashes.safari/">images crashing Safari</a>, this block of code will do it too:<blockquote><code>&lt;html&gt;
&lt;body&gt;

&lt;div&gt;
&lt;div&gt;

&lt;script type="text/javascript"&gt;
document.body.innerHTML = "hello!";
&lt;/script&gt;

&lt;/div&gt;
&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;</code></blockquote>Accidently found that out today... if you want to test it, <a href="http://www.oliverweb.com/crash.php">go for it</a>.