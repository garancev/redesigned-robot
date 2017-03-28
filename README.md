# Git Cheat Sheet

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

## Stashing neatly

To retrieve my stash without being overwhelmed by the stashes later:
```
git stash pop
```
Applies the changes _and_ removes from the pile.

## Sources
When I haven't forgotten the source of my findings already, I'll list them here:

* [Git doc](https://git-scm.com/docs)
* [Andrew Ray's blog](http://blog.andrewray.me/a-better-git-blame/)
