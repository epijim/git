---
title: "Danger zone"
bg: orange
color: black
fa-icon: warning
---

## Destructive commands
<a name="destructive" />

By default, git always has a tracable history. But what happens if you want to jump back to a previous version, or undo work? Git has the commands to do this - and there are valid
reasons to rewrite a history - but for us at Roche "breaking" the timeline and losing information on the history of a file is probably not a good thing (usually it's done just
to make a convuloted history of a repo look prettier).

In github, some of these commands can be blocked from the repo settings, so even if you decide to go backwards, github logs it as steps forward in time to return to a previous state 
(rather than simply deleting your history back to a certain point).

### `reset`
* This takes where you are, and resets time back to a specific commit.
* Jump back two commits, keeping the last two commits in the staged area (so uncommit)
    + `git reset --soft HEAD~2`
* Jump back one commit, but unstage the changes (i.e. pre `git add .`)
    + `git reset --mixed HEAD~`
* Jump back to a specific commit, and remove/discard/delete the changes between now and that commit. This one is deleting the past... so be extra cautious.
    + `git reset --hard 0f5al`
    + Where `0f5al` is the commit hash
* Want to see these commands? The `reflog` stores what's happened in the last 30 days **locally only**. Note - the files may be collected by the bin and deleted earlier.
    + `git reflog` - to see the log
    + `git cherry pick 0g9eo` - jump back to a specific time using the hash from the `reflog`

### `rebase`

If I want to merge two branches, where both have commits, but I don't want the order of commits to be one branch then the others.

* `git rebase -i master`
    + Opens editor, and `pick` the order of the commits, meaning we can do a fast forward merge.
