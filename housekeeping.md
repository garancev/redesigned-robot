# Housekeeping the repo

## Clean up branches

* Check local branches merged with current branch (or without a commit yet):
```shell
git branch --merged
```
* Check local branches not merged with current branch:
```shell
git branch --no-merged
```
Delete _locally_ unwanted branches with `git branch -d <branch_name>`. Force deletion with `git branch -D <branch_name>`  
Delete _remotely_ unwanted branches with `git push origin --delete <branch_name>`  

* Prune references to remote branches that don't exist anymore:  
```shell
git remote prune origin
```
:information_source: Add `--dry-run` to first check what will be deleted !  

# More
* [Studying repo History](studyHistory.md)
* [Fixing mistakes](fixMistakes.md)
* [Fixing conflicts](fixConflicts.md)
* [Stashing](stash.md)
* [My git config](myConfig.md)
* [Meddling with commits](meddling.md)
* [Back to the Readme](README.md).