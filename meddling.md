# Meddling with commits
When I branched off from the wrong branch, and need to change where I come from, I can either create a new branch from the right one, and cherry pick the couple of commits I'm interested in, _or_ I can rebase my branch.

## Cherry-picking several commits
From any given branch, I can pick the commits I want from another branch, by cherry picking.  
To cherry pick A, B, C and D:
```
git cherry-pick A^..D
```
It can recover from merge conflicts just like any other merge, but doesn't recover from merge commits with no message.  

## Rebasing
Another solution is to change the branch I'm based _on_.
A simpler solution is **Rebasing** onto a target branch:
```
git rebase --onto <Branch I want to be starting from> <Commit right before my own commits to rebase>
```
In case of conflict, after fixing it, a simple `add` is enough to fix it, and then `git rebase --continue`.
Giving the commit right before my owns is needed if I already have commits in my own branch. Otherwise, simply the branch name I branched from is enough.

* [Studying repo History](studyHistory.md)
* [Fixing conflicts](fixConflicts.md)
* [Fixing mistakes](fixMistakes.md)
* [Stashing](stash.md)
* [My git config](myConfig.md)
* [Housekeeping the repo](housekeeping.md)
* [Juggling with several git config](severalConfigurations.md)
* [Back to the Readme](README.md).