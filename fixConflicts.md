# Fixing conflicts

## Identifying the conflict
I have a `conflict` command (see [my config](myConfig.md)) to get a diff list with _only_ the conflicted files.
## No brainer conflicts
When I know who has the truth, I can use one of the following commands:

```shell
git checkout --theirs index.html
git checkout --ours index.html
```

If one of the file's state is deleted, and that's what I want to keep, I have to :

```
git rm index.html
```

## Medium conflicts

If conflicts are localised enough (eg no functions were moved around the file, not 10 files with a conflict), I can fix them by hand, always remembering what the conflict marks mean:

```javascript
<<<<<<< Updated upstream / HEAD
       `The code in between <<<<<<< and ======= is the new code, the code from remote, from the applied stash or from the other branch I wanted to merge into mine.`
=======
      `The code in between ======= and >>>>>>> is *my local code*, what I just wrote myself / what was already in the branch I'm currently on. `
>>>>>>> Stashed changes / Branch-name
```


## Extreme conflicts

For those cases, a visual tool helps! (then I envy people using git with their IDE).
Luckily, we have visual tools in git command line too. :tada:
_...in construction..._

# More
* [Studying repo History](studyHistory.md)
* [Fixing mistakes](fixMistakes.md)
* [Stashing](stash.md)
* [My git config](myConfig.md)
* [Housekeeping the repo](housekeeping.md)
* [Meddling with commits](meddling.md)
* [Back to the Readme](README.md).