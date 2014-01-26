---
title: git commands
layout: default
---
{{page.title}}
==============

add parts of a file
-------------------

[Stack overflow][partial add] says:

```bash
git add -p [filenane]
```

Find differences
----------------

[Stack overflow][diffs answer] says:
![Diagram explaining the diffs between HEAD, Index and Working tree][diff diagram]

### HEAD -> Index (staging area):

```bash
git diff --cached
```

### Index (staging area) -> Working Tree

```bash
git diff
```

### HEAD -> Working Tree

```bash
git diff HEAD
```

[partial add]: https://stackoverflow.com/questions/1085162/how-can-i-commit-only-part-of-a-file-in-git
[diff diagram]: http://images.abizern.org.s3.amazonaws.com/365git/March10/GitDiffSimple.png
[diff answer]: http://stackoverflow.com/a/1587952/189995
