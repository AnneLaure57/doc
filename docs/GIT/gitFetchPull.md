# How to fetch all Git Branches

to git fetch your all branchs, you can use this :

```
git fetch --all
git pull --all // update your local branches
```

fetch updates local copies of remote branches so this is always safe for your local branches BUT:

- fetch will not update local branches (which track remote branches); if you want to update your local branches you still need to pull every branch.

- fetch will not create local branches (which track remote branches), you have to do this manually. If you want to list all remote branches: git branch -a

https://www.atlassian.com/git/tutorials/syncing/git-fetch

https://stackoverflow.com/questions/10312521/how-to-fetch-all-git-branches 

https://www.google.com/search?q=difference+between+git+fetch+and+git+pull&rlz=1C1GCEU_frLU970LU970&sxsrf=AOaemvIo_I-bRWlHJDfVTLnbjsD5y0tNUA:1639732130444&source=lnms&tbm=isch&sa=X&sqi=2&ved=2ahUKEwjFo6WZvur0AhVeVTABHVQICosQ_AUoAXoECAgQAw&biw=1536&bih=722&dpr=1.25#imgrc=6dDmpRixtHCitM