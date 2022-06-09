# How use git move ?

```
mv oldname newname
git add newname
git rm oldname
```

Git has a rename command git mv, but that is just a convenience. The effect is indistinguishable from removing the file and adding another with different name and the same content.

Sources :

https://stackoverflow.com/questions/1094269/whats-the-purpose-of-git-mv