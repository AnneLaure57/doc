# COnfigure GIT Portable for Windows

## What is GIT Portable ?

GIT Portable is a tool, allow to install GIT on your laptop, for Windows.

## Installation

* [GIT - Installaltion](https://git-scm.com/download/win)

Unzip the `.zip` repo and install in the root of your directory.

When is it done, check your git version with the next command :

```
git --version
```

## Generate your SSH keys

In your User directory, create the ´.ssh´ directory :
```
mkdir .ssh
```

Puis
```
cd .ssh
```

et vous tapez :

```
ssh-keygen
```

A public and a private keys will be generated.
## Test your installation

You can test with the next command, to clone a remote repository :

HTTP / SSH

```
git clone <your remote git>
```
## Useful commands GIT

```
git add -A (add all files updated) // -A : all . = add entire directory recursively
git commit -(a)m <message>
git push (push your commit)

git pull (recover the modifications of the deposit, to be done as often as possible to avoid mergers)

git status (have information about the repository such as commits, branches etc)

git log

git log --graph --oneline --decorate (get graphic representation)

git reflog (allows to have the history and the symbolic reference HEAD)

git merge (make a merge)

git branch <branch> (create new branche)

git checkout <branch> (change branch)

git checkout -b <newBranch> <oldBranch>
```
