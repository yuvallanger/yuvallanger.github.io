---
title: IRC Commands
layout: default
---
commonly-forgotten
==================

{{ page.title }}
==================

Jerks
-----

In case of flooding jerks, use this (quiet the unregistered):

```IRC
/mode +q $~a
```

In case of many sock puppet jerks join-flooding, use this (only registered users can join):

```IRC
/mode +r
```

No Jerks
--------

In case of no jerks, use these:

```IRC
/mode -rq $~a
```

Flags
-----

* `+q` - `q`uiet - like `+b` but instead of banning, it silences.
* `+r` - `r`egistered - restricts joining to registered users.

ExtBans
-------

* Extended syntax for bans.
* Added to `+q` or `+b` instead of regular `foo!bar@quux`

* $a - registered (`a`ccount)
* ~ - negation
