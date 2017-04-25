# Studying repo History
## History of a file
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

## About one commit
* To see only a list of the files changed in the commit, instead of each diff:  
```
git show <hash> --name-only
```


[Next: Fixing mistakes](fixMistakes.md).
[Back to the Readme](README.md).
