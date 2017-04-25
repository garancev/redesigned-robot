# My git config
My global git config (`~/.gitconfig`)is in this repo as `global-gitconfig`. It has different parts:
## Aliases
Convenience aliases, for the operations I do 50 times a day:  
`git st = git status`  
`git ch = git checkout`  
`git pl = git pull`  
`git ph = git push`  
`git a = git add`  

## Log
To print my git logs with a default level of reading comfort, the `abrevCommit` flag is true by default.

# Hooks

## Pre-commit
See the `pre-commit` file, which, in my setup, lives in ~/.git-templates/hooks  
I am aborting commits where modified files contain unwanted elements, such as TO~DOs.
That's a general rule, no matter the git repository.

## Post-commit
I haven't found a use for post-commit yet.

[Next: Housekeeping the repo](housekeeping.md).
[Back to the Readme](README.md).