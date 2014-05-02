---
layout: default
title: Commands I infrequently need.
---
{{ page.title }}
=============================

HOWTO: Use mplayer to rip video streams
---------------------------------------
Dump streams, vlecs (personal use, of course), videos - mplayer -dumpfile [file] -dumpstream [url]

HOWTO: Detach another byobu connection
--------------------------------------

`ctrl-a ctrl-D`

Clean up a text file
--------------------
From https://stackoverflow.com/questions/12999651/how-to-remove-non-utf-8-characters-from-text-file
specifically from http://stackoverflow.com/a/17048486/189995

`iconv -f utf-8 -t utf-8 -c file.txt`
