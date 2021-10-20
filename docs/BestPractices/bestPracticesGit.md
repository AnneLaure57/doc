# Best Pratices Git

last update : 20/10/2021

Advice  :

## **1 - Don't ```git push ``` straight to master** 

-> keep your code safe and deployable any time.

Description : 

<p style="text-align:justify;"> Use the concept of "cheap branching". Use differents branch promote the collaboration, and allow to ignite heathly discussions, improve
codebase quality and spread the knowledge with others developpers (Code Review).</p>

```
git branch -b <name> master // create new branch from master

git checkout - //switch back to the previous branch
```

### **1.1 - Use the branch naming convention**

<p style="text-align:justify;">Adopting a consistent branch naming convertion is essential to keeping your repository. The most popular ones is "git flow".</p>

![Screenshot](../images/gitflow.png)

[![Generic badge](https://badges.aleen42.com/src/github.svg)](https://nvie.com/posts/a-successful-git-branching-model/)


## **2 - Don't commit the code as an unregognized author**

Description : 

<p style="text-align:justify;"> Use for keep a trace of the developpment, who developp what. Example, it's possible to use the command :</p>

```
git blame <file>
```

### **2.1 - write descriptive and meanungful commit messages**

![Screenshot](../images/listTipsGit.png)

Apply the **SOLID** concept -> S -> Single Responsibility Principle.

push the least amount of lines thaht make sens together.

## **3 - Define code owners for faster code reviews**

Use the *Code Owners* feature to define which teams and people are automatically selected as reviewers.

link to doc [![Generic badge](https://badges.aleen42.com/src/github.svg)](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

## **4 - Don't leak secrets into source control**

Secrets : account passwords, API keys, private tokens, SSH Keys ...

Possiblity to use **Hashicorp Vault** or **AWS Secrets Manager**

If you want check your repository, you have the possibility to use tools for scanning secrets and prevent attack or theth data.

* Git-secrets : identify in your code
* Git hooks : can be used to build a pre-commit hook and check every pull request for secrets

Available on the web.

## **5 - Don't commit dependencies or local config files**

If you push your project dependencies on your remote repository, it will be increase your repository size.
For the config files, the best way is to defne the elements on your ```.gitignore```.

link to doc [![Generic badge](https://badges.aleen42.com/src/github.svg)](https://www.toptal.com/developers/gitignores)

## **6 - Archive dead repositories**

## **7 - Lock package versions**

## **8 - Specify standard package versions**

## **9 - Levrage task list**

Way for the *totrack to-dos* in ```.md```  files. The Tasks lists provide an excellent way to capture a high-level overview of a task or issue.

## **10 - Keep branches up to date**

You pull from remote, hit merge and suddently you're faced with a barrage of merge conflicts.
The best practice here is to ensure that you’re consistently merging your base branch into your current branch as you work, especially if it’s a long-outstanding branch.

## **11 - Enable security alerts**

Possibility to track reported security vulnerabilities in some dependencies and will even suggest fixes for your projects.
[![Generic badge](https://badges.aleen42.com/src/github.svg)](https://docs.github.com/en/code-security/supply-chain-security/managing-vulnerabilities-in-your-projects-dependencies/about-alerts-for-vulnerable-dependencies)

## **12 - Rebase your working branch frequently**

```
git checkout <upstream_branch>

git pull

git checkout -

git rebase <upstream_branch>
```

or 
```
git fetch --prune
```

## Useful commands

```
git log 

git blame 

git cherry-pick

git diff and git apply

git stash

git bisect

git push -u | --set-upstream origin <branch>

git push --force | -f <branch> // rewrite the history

git rebase -i // remove branch history

```

## Sources

* [Datree](https://www.datree.io/resources/github-best-practices)
* [sourcelevel.io](https://sourcelevel.io/blog/7-git-best-practices-to-start-using-in-your-next-commit)