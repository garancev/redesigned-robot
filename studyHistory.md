# Studying repo History
## Files history
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

## About one commit
* To see only a list of the files changed in the commit, instead of each diff:  
```shell
git show <hash> --name-only
```


# More
* [Fixing mistakes](fixMistakes.md)
* [Fixing conflicts](fixConflicts.md)
* [Stashing](stash.md)
* [My git config](myConfig.md)
* [Housekeeping the repo](housekeeping.md)
* [Back to the Readme](README.md).
