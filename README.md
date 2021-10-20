# memo-git https://training.github.com/downloads/fr/github-git-cheat-sheet.pdf

What does mean remote github?
Git Remote = Git repository that’s hosted on the Internet or another network
https://www.gitkraken.com/learn/git/tutorials/what-is-git-remote

What does mean origin github?
"origin" is just what you nicknamed your remote repository when you ran a command like this:

git remote add origin git@github.com:USERNAME/REPOSITORY-NAME.git
https://stackoverflow.com/questions/9529497/what-is-origin-in-git

Origin fait partie des remote repository en quelque sorte et il n'y a pas de "surnom" pour le repository local

Les différences entre Git et GitHub :
Git est un programme de lignes de commandes pour gérer les versions (branches) d'un projet. GitHub est le site web où l'on peut partager son projet avec d'autres personnes et travailler avec eux (pull de leurs commits, et on push les notres) en gardant une même branche principale : la branche origin du repo à distance ; et en faisant des modifications sur des branches annexes qui viendront alimenter la branche origin en respectant les "to do" : les issues.
___
Pour changer le mot de passe et changer de compte ou "logout from Git bash and login it again as another user"
Recherches Google "log in in git" "log out git" et ainsi il y a deux manière :
- via le Credentials Manager
cf https://stackoverflow.com/questions/56573522/how-can-i-login-to-git/56573696

- via la commande git Bash
rundll32.exe keymgr.dll, KRShowKeyMgr
cf https://stackoverflow.com/questions/23740734/logout-and-login-as-another-user-git-bash

- la piste non aboutie https://stackoverflow.com/questions/3860112/multiple-github-accounts-on-the-same-computer puis https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


étape 1 
* pouvez vérifier que Git existe vraiment en tapant:
  * git --version
* Définissez votre nom:
  * git config --global user.name "Your Name"
* Maintenant configurez votre courrier électronique:
  * git config --global user.email "youremail@example.com"


étape 2
* Créer un nouveau dossier (aka make directory)
  * mkdir <<FOLDERNAME>>
* Créer un nouveau fichier
  * touch <<FILENAME>>
* Naviguer dans un dossier existant (aka change directory)
  * cd <<FOLDERNAME>>
* Lister les éléments dans un dossier
  * ls
* Activez Git pour un repertoire
  * git init


étape 3 

* Vérifiez l'état des modifications dans un dépôt
  * git status
* Afficher les modifications apportés aux fichiers
  * git diff
* Ajouter les modifications d'un fichier à soumettre
  * git add <<FILENAME>>
* Pour ajouter toutes les modifications d'un seul coup
  * git add .
* Pour soumettre les modifications que vous avez ajoutées avec un court message décrivant les modifications
  * git commit -m "your commit message"

  
étape 4 
* Ajoutez votre nom d'utilisateur GitHub à votre configuration Git:
  * git config --global user.username <<USerNamE>>
* Vous pouvez vérifier ce que vous avez configuré dans Git en tapant: :
  * git config --global user.username

étape 5 
  * git push
  * git pull
* pour merger (en se placant sur la branche main et pour ramener les changements de test2 vers main)
  * git merge test2
 
 étape ignorer
* éviter que les vidéos et autres gros fichiers soit compter sur GitHub :
  1. mettre à la racine du repo **.gitignore** (pas .gitignore.txt qui ne marche pas) 
  2. mettre les documents concerné dans le document .gitignore 
    * .mp4
    * video.mp4
    * dossier/ (écrire / pour signifier le dossier)
 
 ___
 
Autres lignes de commande Julien 
* pour afficher le chemin d'un dossier/fichier
  * pwd
* ls -al
raccourci de :
  * ls -l
  * ls -a (pour voir les fichiers cachés)
* pour effacer le fichier .git (rm pour remove)
  * rm .git pour effacer le fichier .git 
  * rm -rf .git
r pour récursif, f pour forcé

* afficher la liste des url remote
  * git remote
  * git remote -v, pour afficher plus en détail
 
* pour supprimer le lien entre le remote et le local
  * git remote remove origin

* pour recréer un lien entre le remote et le local
  * git remote add origin <url https sur github>
 
* View Contents of Multiple Files in terminal
  * cat test test1
https://www.tecmint.com/13-basic-cat-command-examples-in-linux/
  * cat cookie.md

 * pour renommer une branche
   * git branch -M <<nouveau nom de branche>>

 ---
 * supprimer branche 
   * git branch -d <<autreBranch>>
 * créer branche (sans aller dessus)
   * git branch <<autreBranch>>
 * pour aller sur un commit particulier ou une autre branche  
   * git checkout <<>>
 * créer branche et aller dessus
   * git checkout -b <<autreBranch>>
 * changer de branche (checkout aussi mais switch est plus clair et évite la confusion)
   * git switch <<autreBranch>>
 
 * voir les log avec les barres verticales et les étoiles
   * **git log --oneline --decorate --graph**

------------------------------------------------------

Julien
 
 git diff pour voir les anciennes modifications entre deux commit
 * pour effacer les changements qu'on a fait dans la branche et revenir à la base
   * git reset --hard HEAD
 * j'ai fait des changements, je garde en brouillon et je change de branche pour aller voir des choses ailleurs et laisser tel quel
   * git stash (puis les changements disparaissent c'est normal, puis on change de branche)
 * je reviens sur la branche brouillon et je unstash
   * git stash pop
   * autre manière git commit -a -m ""
 
------------------------------------------------------
 
message erreur : LF will be replaced by CRLF
  * git config --global core.autocrlf false
https://qastack.fr/programming/17628305/windows-git-warning-lf-will-be-replaced-by-crlf-is-that-warning-tail-backwar

