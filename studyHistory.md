# Studying repo History

## What did I just do ? :fearful:

To see the difference between HEAD and the staged files:
```shell
git diff --staged
```

To check everything I recently did:
```shell
git reflog
```
It also gives a reference to each passed state, that I can checkout same as if it was a stash.
It is in fact a built-in alias of `git log -g --abbrev-commit --pretty=oneline`.

## File history
### Git blame  
`Git blame` is nice, when I know what I'm looking for.  
I can even specify line ranges:  
```shell
git blame -L <start>,<end> <file>
```

### Git log  
Depending on the situation, I use `git log` with different options.  
* To see a general history of the file I'm looking for:  
```shell
git log -p -M --follow --stat -- <file>
```

* To see when a specific expression was removed or added:  
```shell
git log -GexpressionILookFor
```  

## Commit history
* To see only a list of the files changed in the commit, instead of each diff:  
```shell
git show <hash> --name-only
```

* To see all the commits by one specific person:
```shell
git log --pretty=format:"%ad:%an:%d:%B" --date=short --branches --since=2.months.ago --author="git Username"
```


# More
* [Fixing mistakes](fixMistakes.md)
* [Fixing conflicts](fixConflicts.md)
* [Stashing](stash.md)
* [My git config](myConfig.md)
* [Housekeeping the repo](housekeeping.md)
* [Back to the Readme](README.md).
