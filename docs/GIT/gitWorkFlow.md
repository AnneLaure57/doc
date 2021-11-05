## GIT workflow

Git cherry-pick
rebase
merge

```
git checkout master
git pull origin master
git merge --no-ff test
git push origin master
```



## Merge

### Git Flow : Fast-forward and no fast-forward

<p style="text-align:justify;">git will (by default) do what is known as a fast-forward merge; master's branch pointer is just updated to be the same commit as the tip of your merge. This usually results in a simpler commit history that is easier to work with, especially if work is also going on in remote repositories.</p>

In this case, use :

```
git merge --no-ff <branch>
```

<p style="text-align:justify;">It's generally considered like a best practice to keep the version history as topologically simple as possible, which means to use fast-forward. The <b>--no-ff</b> option is there to support methodologies that demand explicit branching and merge tracking.</p>

[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/16217363/git-graph-not-showing-branch)

* ```--no-ff``` : no fast-forward
* ```--ff-only``` : fast-forward

Quote : git pull -> equivalent --ff-only

## Rebase

Links
https://www.google.com/search?q=difference+between+merge+and+cherry+pick&rlz=1C1GCEU_frLU970LU970&oq=difference+between+merge+and+che&aqs=chrome.0.0i19j69i57.11035j0j7&sourceid=chrome&ie=UTF-8
https://www.codeproject.com/Tips/5260897/Advanced-GIT-Tutorial-Cherry-Pick-vs-Rebase-vs-Mer
https://stackoverflow.com/questions/1241720/git-cherry-pick-vs-merge-workflow
https://www.previousnext.com.au/blog/intro-cherry-picking-git
https://anexinet.com/blog/git-practical-aspects-of-merge-rebase-cherry-pick/
https://igomobile.de/2018/05/23/difference-between-merge-and-cherry-pick-in-git/
https://stackoverflow.com/questions/53972594/what-is-the-difference-between-a-git-merge-and-git-cherry-pick-for-a-specific-co/53972713
https://www.google.com/search?q=best+practise+merge+branch&rlz=1C1GCEU_frLU970LU970&oq=best+practise+merge+branch&aqs=chrome..69i57j0i22i30l2j0i8i13i30l2.6760j0j7&sourceid=chrome&ie=UTF-8
https://gist.github.com/calaway/ea880263b0c0495bb00ee877f001dc59
https://stackoverflow.com/questions/5601931/what-is-the-best-and-safest-way-to-merge-a-git-branch-into-master
https://www.google.com/search?rlz=1C1GCEU_frLU970LU970&sxsrf=AOaemvK-LbcHXJA8Tc7HuTq9WSjPYr8XWw%3A1636007105771&lei=wXyDYfq-LsvTkwWbhorIDg&q=git%20merge%20--no-ff&ved=2ahUKEwi6o46zif7zAhXL6aQKHRuDAukQsKwBKAB6BAg0EAE&biw=1536&bih=722&dpr=1.25
https://stackoverflow.com/questions/9069061/what-is-the-difference-between-git-merge-and-git-merge-no-ff
https://www.google.com/search?q=cherry+pick+git&rlz=1C1GCEU_frLU970LU970&sxsrf=AOaemvJuzsU87VRCDgASkXkrMAMlEv14Iw:1635947474976&source=lnms&tbm=isch&sa=X&ved=2ahUKEwid9Pagq_zzAhXVh_0HHdvBAgAQ_AUoAXoECAEQAw&biw=1536&bih=722&dpr=1.25
https://nvie.com/posts/a-successful-git-branching-model/