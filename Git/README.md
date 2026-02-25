# Formation Personnelle Git

## Configuration des paramètres d'utilisateur
- Nom d'utilisateur : `git config --global user.email "wilsonnguiffo@gmail.com"`
- Adresse courriel : `git config --global user.name "Wilson Junior"`
- Couleur : `git config --global color.ui true`
- Etat de la configuration git : `git config --list`

## Commits
- Commits et ajout direct : `git commit -a -m "message"`
- Pour controller les commits : `git log`
- Pour controller un  nombre m de commit : `git log -n m`
- Pour controller les informations essentielles d'un certain nombre de commit: `git log --oneline -n m`
- Pour controller les informations essentielles d'un certain nombre de commits concernant un fichier en particulier (index.html) : `git log --oneline -n m -p index.html`
- Différence entre le fichier commité et le fichier modifié : `git diff`

## Revenir en arrière

- Pour revoir l'état précédent du fichier index.html, faire d'abord un : **git log --oneline index.html**
- Pour voir en spectateur l'état d'un commit à un moment donnée précédent, faire un : ``` git checkout (clé ssh1 du commit ex : e32bb29) ```
- Pour revenir dans l'état de base, faire un ``` git checkout main ```
- La commande ```revert``` permet de defaire ce qui a été fait à un commit en particulier : ```git revert e32bb29``` défait ce qui a été fait à ce commit; Pour défaire le revert, faire un revert avec la clé du revert précédent.

## Les branches

- Creation des branches : ```git branch (nom de la branche)``` ex : ```git branch design```
- Pour passer à une autre branche : ```git checkout design```
- Pour ajouter les modifications faites sur les autres branches (pour faire une fusion), on se place sur la branche sur laquelle on souhaite rapatrier l'autre branche et on utilise la commande ```git merge (nom de la brange à faire fusionner)``` ex : étant sur la branche main et voulant ajouter les modifications de la branche redesign à la branche main, on utilise la commande ```git merge redesign```
- Pour supprimer une branche : ```git branch -d redisgn```
---
**La commande Reset**
- ```--hard``` modifie l'historique et retourne tout le code à l'état du commit utilisé dans le reset (supprime les modifications) : ```git reset HEAD^ --hard```
- ```--soft``` reviens en arrière, sans modifier le fichier et **add .** tous les fichiers
- ```--mixed``` reviens en arrière sans faire le **add .**
- pour revenir de ```n``` niveau de commit, mettre **n fois** ```^``` devant le ```HEAD``` : ```git reset HEAD^^ --soft```
- La simple commande ```git reset HEAD``` est équivalente à un ```git reset HEAD -- mixed```

# UNGIT

## Installation

1. Installer ```node.js```
2. dans le terminal à partir du repertoire du projet, lancer ```npm install -g ungit```
3. Ensuite à partir du terminal, lancer la commande ```ungit```
4. Si une erreur apparait dans le terminal, lancer la commande ```set UNGIT_DISABLE_WATCH=true``` puis relancer ```ungit```