# Stashing
Stashing is great, _if_ I can retrieve what I want, when I want it. I still miss one feature, getting a bell rang when I get to a branch where something is stashed, to avoid re-doing things... If anyone has a clue!

## Creating a stash
I usually simply `git stash`, but there are better ways. Namely, giving a message to my stash, to know what it's about:  
```shell
git stash save -- "stash message"
```
I have an alias for that command, `git keep "message"`. 

## Finding the right stash
Get the list of all stashs:
```
git stash list
```
The result:
```shell
stash@{0}: WIP on feature/JIRAFeature1: da9c40171b Last commit message on head at the time
stash@{1}: WIP on feature/JIRAFeature1: 91c8ae2a88 Last commit message on head at the time
```

## Applying the right stash
My default command to apply the latest stash:
```shell
git stash pop
```
Applies the changes _and_ removes them from the pile.  


Applying a stash with its identifier directly (if it's not the latest one):
```
git stash apply 1
```

:information_source: the old git versions need `"@stash{1}"` instead of directly `1`.  
:information_source: With the long version, I need the quotes because I'm using zsh. A regular bash doesn't need them.

Applying a stash can lead to a conflict just the same way as a merge. (See [fixing conflicts](fixConflicts.md))

Removing a stash from the stash list:
```
git stash drop 1
```



# More
* [Studying repo History](studyHistory.md)
* [Fixing mistakes](fixMistakes.md)
* [Fixing conflicts](fixConflicts.md)
* [My git config](myConfig.md)
* [Housekeeping the repo](housekeeping.md)
* [Back to the Readme](README.md).