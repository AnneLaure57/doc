How undo a git rm ?

If it's the last commit, you can try this :

```
git commit --amend / -a
```

Else 

```
git reset --soft HEAD~N
git status
```

https://stackoverflow.com/questions/33983138/how-to-undo-git-rm