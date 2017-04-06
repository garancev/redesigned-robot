# Git Cheat Sheet

## Studying repo History
### History of a file
* Git blame  
`Git blame` is nice, when I know what I'm looking for.  
I can even specify line ranges:  
```
git blame -L <start>,<end> <file>
```

* Git log  
Behold, `git log` to see a more general history of the file I'm looking for:  
```
git log -p -M --follow --stat -- <file>
```

### About one commit
* To see only a list of the files changed in the commit, instead of each diff:  
```
git show <hash> --name-only
```


## Stashing neatly
To retrieve my stash without being overwhelmed by the stashes later:
```
git stash pop
```
Applies the changes _and_ removes from the pile.


## Fixing mistakes
Sometimes I do dumb stuff, or _radically_ change my mind on the best way to solve a problem, and want to remove the previous version from history.  
This can only work if absolutely no one else is working on my branch.

### Undoing local stuff
Soft reset of the last commit:
```
git reset HEAD~
```
` ~ `  means commit before last  
Soft because all the changes will still be in my repo, I can do whatever I want with them.  
To completely get rid of my local commits and changes, and get back to the remote branch HEAD, I can;
```
git reset --hard origin/<branch_name>
```
Reset always needs a commit to refer itself to.

### Undoing remote stuff
I have the bad habit of not seeing my biggest mistakes on the repo, _especially_ if I know how to fix them right after I made them!
(the real bad habit is to not think enough before pushing :grin: )
I haven't been in this situation since I started this document, so no command yet.

## My git config
My global git config (`~/.gitconfig`)is in this repo as `global-gitconfig`. It has different parts:
### Aliases
Convenience aliases, for the operations I do 50 times a day:  
`git st = git status`  
`git ch = git checkout`  
`git pl = git pull`  
`git ph = git push`  
`git a = git add`  
### Log
To print my git logs with a default level of reading comfort, the `abrevCommit` flag is true by default.

## Hooks

### Pre-commit
See the `pre-commit` file, which, in my setup, lives in ~/.git-templates/hooks  
I am aborting commits where modified files contain unwanted elements, such as TO~DOs.
That's a general rule, no matter the git repository.

### Post-commit
I haven't found a use for post-commit yet.

# Sources
When I haven't forgotten the source of my findings already, I'll list them here:

* [Git doc](https://git-scm.com/docs)
* [Andrew Ray's blog](http://blog.andrewray.me/a-better-git-blame/)
* [StackOverflow answer by underrun for git flags](http://stackoverflow.com/a/11884798/6329359)