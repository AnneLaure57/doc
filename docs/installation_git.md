# Configurer GIT Portable pour Windows

## Qu'est-ce que GIT Portable ?

GIT Portable est une version ne demandant pas les droits administrateurs pour installer GIT sur votre machine Windows.

## Installation

* [GIT - Installaltion](https://git-scm.com/download/win)

Dézipper ensuite le `.zip` et installer à la racine de votre répertoire.

Une fois que c'est fait, vérifier votre version de git.

```
git --version
```

## Ajouter le chemin dans la variable d'environnement PATH

Aller dans vos variables d'environnement et rajouter le chemin /bin ou /user/bin/ (on s'en fout un peu), pour que Windows puisse vous générer votre paire de clés dans le répertoire **/.ssh**.

![répertoire ssh](/images/path.png)

## Génération de votre paire de clés SSH

Dans votre répertoire **/votre-NNI** , créer un répertoire .ssh (en ligne de commandes):
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

Vous aurez alors une clé publique (id_rsa_pub) et une privée (id_rsa).

## Fichier Config

N'oublier pas d'ajouter dans ce répertoire <span style="color: #26B260">*ssh*</span> un fichier config qui vous permettra d'utiliser git avec GitLab (le port 22 étant bloqué).

fichier `config` (disponible dans le même dépôt).

```
Host devcattenom
	Port 50002

Host 10.168.24.224
    Port 50002
```

Voici ce que l'on retrouve dans le répertoire /.ssh :

![répertoire ssh](/images/ssh.png)

## Tester votre configuration

Vous pouvez tester en essayant la commande suivante :

HTTP

```
git clone yourGit
```

SSH

```
git clone yourGit
```

ou le faire dierectement depuis GitLab.

Vous aurez alors le répertoire `gitlab_documentation` de cloner dans le répertoire dans lequel vous avez exécuté la commande.

<span style="color: #ff1a00"> En cas de problème, No Panic ! </span> Demande à ton voisin un coup de main contre une bonne binouse,</span> sinon [readthedocs](https://guides.github.com/activities/hello-world/).

## Commandes GIT utiles

```
git add -A . (ajouter seulement les fichiers qui ont été modifiées)
git commit -(a)m "votre message de commit"
git push (envoyer votre commit)

git pull (récupérer les modifications du dépôt, à faire le plus souvent possible pour éviter les fusions)

git status (avoir des informations sur le dépôt telles que les commits, branches etc)

git log
git log --graph --oneline --decorate (représentation sous format graphique)

git reflog (permet d'avoir l'historique et la référence symbolique HEAD)

git merge (faire un merge)

git branch nom-de-votre-branche (créer une branche)

git checkout nom-branche (se placer sur une autre branche)
```
