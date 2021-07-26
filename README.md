# memo-git

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
