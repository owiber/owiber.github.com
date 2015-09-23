---
author: Oliver
comments: true
date: 2009-08-02 05:22:44+00:00
excerpt: None
layout: post
slug: applescript-itunes-ichat
title: AppleScript + iTunes + iChat
wordpress_id: 746
tags:
- nerdy
- weekend
---

I ran across this <a href="http://maketecheasier.com/mac-osx-remote-control-your-itunes-via-ichat/2008/04/18">nifty little blog post</a> that lets you control a remote Mac's iTunes via iChat.  I decided to customize the script a bit and added a way to search for songs.  Here's my addition to the stock AppleScript:

<pre>
else if (theMessage begins with "song " and theMessage is not "song ")
     or (theMessage begins with "s " and theMessage is not "s ") then

    set cLength to (count (first word of theMessage)) + 1
    set query to texts cLength thru -1 of theMessage

    tell application "iTunes"
        set theSongs to (search playlist "Library" for query)
        try
            set songID to persistent ID of (item 1 in theSongs)
            play (first track of (get some playlist whose special kind is Music)
                 whose persistent ID = songID)
            set theResponse to "Playing song request. "
        on error
            set theResponse to "Did not find any songs. "
        end try

    end tell

    set theResponse to theResponse & getCurrentiTunesTrack()
</pre>

I also added "aliases" to the previous and next commands ("p" and "n" respectively), but that was pretty trivial, so I won't include it here.  This is the first AppleScript I've written, so I'm probably making some noobish mistakes, but it was pretty cool.  Now I can chat with my Mac Mini and tell it what to play!

<img src="https://www.owiber.com/wp-content/uploads/2009/08/ichatitunes.png" alt="AppleScript/iTunes/iChat" title="AppleScript/iTunes/iChat" width="359" height="386" class="alignnone size-full wp-image-749 noborder" />