# Housekeeping the repo

## Clean up branches

* Prune references to remote branches that don't exist on remote anymore:  
```
git remote prune origin
```
Add `--dry-run` to first check what will be deleted !  
* Check local branches merged with current branch (or without a commit yet):
```
git branch --merged
```
* Check local branches not merged with current branch:
```
git branch --no-merged
```
Delete unwanted branches with `-d`. Force deletion with `-D`  s


[Back to the Readme](README.md).