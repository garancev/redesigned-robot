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

### Undoing remote stuff
I have the bad habit of not seeing my biggest mistakes on the repo, _especially_ if I know how to fix them right after I made them!
(the real bad habit is to not think enough before pushing :grin: )
I haven't been in this situation since I started this document, so no command yet.

## My git config
### Aliases
`git log --abbrev-commit` as an alias of git log

### Hooks

#### Pre-commit
 See the `pre-commit` file, which, in my setup, lives in ~/.git-templates/hooks  
I am aborting commits where modified files contain unwanted elements, such as TO~DOs.
That's a general rule, no matter the git repository.



# Sources
When I haven't forgotten the source of my findings already, I'll list them here:

* [Git doc](https://git-scm.com/docs)
* [Andrew Ray's blog](http://blog.andrewray.me/a-better-git-blame/)
