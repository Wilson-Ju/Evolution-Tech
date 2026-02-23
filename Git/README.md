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