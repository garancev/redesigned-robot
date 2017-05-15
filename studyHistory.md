# Studying repo History
## Files history
### Git blame  
`Git blame` is nice, when I know what I'm looking for.  
I can even specify line ranges:  
```
git blame -L <start>,<end> <file>
```

### Git log  
Depending on the situation, I use `git log` with different options.  
* To see a general history of the file I'm looking for:  
```
git log -p -M --follow --stat -- <file>
```

* To see when a specific expression was removed or added:  
```
git log -GexpressionILookFor
```  

## About one commit
* To see only a list of the files changed in the commit, instead of each diff:  
```
git show <hash> --name-only
```


[Next: Fixing mistakes](fixMistakes.md).  
[Back to the Readme](README.md).
