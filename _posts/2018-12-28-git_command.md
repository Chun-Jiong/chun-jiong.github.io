---
layout: post
title: "A collection of git commands (will continue to update)"
date: 2018-12-28
modified: 2018-12-28
---

> Build  28 Dec 2018
> Modify 28 Dec 2018

### git bisect

git bisect - Use binary search to find the commit that introduced a bug

1. start git bisect and set the region
- git bisect start [end hash point] [start hash point]

2. mark good or bad
- At this time, the repository will be checkout to the middle point of the setting region
- Check this repository is good or bad
> if good, execute: git bisect good. That is to say the bug is in the second-half commit
and it will locate the repository to the middle point of the second-half region.
> if bad, execute: git bisect bad. That is to say the bug is in the first-half commit
and it will locate the repository to the middle point of the first-half region.

3. repeat progress 2
- Utill find the bad commit and git will give the hash value of the bad commit.

4. fix the bug
- now it is the time to fix the bug.

The Chinese tutorial can be find in [here](http://www.ruanyifeng.com/blog/2018/12/git-bisect.html).
