---
author: Oliver
comments: true
date: 2005-11-16 07:10:18+00:00
excerpt: None
layout: post
slug: done-with-ubuntu-reinstall
title: Done with Ubuntu Reinstall
wordpress_id: 166
tags:
- linux
---

Since I know I'll be looking for this info again the next time I reinstall (maybe)... here goes some info dump:

/etc/inetd.conf:
<blockquote>netbios-ssn     stream  tcp     nowait  root    /usr/sbin/tcpd  /usr/sbin/smbd
swat            stream  tcp     nowait.400      root    /usr/sbin/tcpd  /usr/sbin/swat
vnc     stream  tcp     nowait  nobody  /usr/bin/Xvnc Xvnc -inetd :10 -broadcast -desktop=Nibbler -once securitytypes=none -fp /usr/share/X11/fonts/misc -depth 24 -geometry 1024x768
cvspserver      stream  tcp     nowait  cvs     /usr/bin/cvs cvs -f --allow-root=/cvs pserver</blockquote>

/etc/services:
<blockquote>vnc             5900/tcp #VNC &amp; GDM
cvspserver      2401/tcp</blockquote>

Notes: Have both vncserver and vnc4server packages installed, but I think vnc4server overwrote the old version.

/etc/fstab:
<blockquote>/dev/hda3       /mnt/macosx     hfsplus users,rw,auto,exec      0 0</blockquote>

Ummmm... that's all for now. =)