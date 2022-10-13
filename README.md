# revision-git

Quelques exercices pour apprendre à prendre en main git !

## Exercices

### 0 Installation

Installer git sur votre pc :

- windows : http://git-scm.com/download/win
- linux (ubuntu/debian) : sudo apt get install git -y

### 1 Basics

1. Récupérer l'url HTTPS  de ce dépôt sur github (cliquer sur le bouton vert code).
2. Avec la commande git clone, cloner ce depot git.
3. Aller dans le dossier en local et lancer ls -la. Vérifier que les fichiers présents sont identiques au depot distant
4. la commande git status permet de savoir si des fichiers ont été modifié depuis la derniere sauvegarde dans git. Lancer git status
5. Créer un fichier dont le nom est votre prénom ou username
6. lancer la commande git status. Lire le message.
7. Avec la commande git add ajouter le fichier pour qu'il soit ajouté dans le prochain commit.
8. faire un git status. Qu'est ce qui a changé ? 
9. Valider la sauvegarde du commit avec la commande git commit. Faire en sorte que le message du commit soit   "mon premier commit"
10. Faire un git log pour vérifier que le commit a bien été ajouté à l'historique des commits
11. lancer à nouveau git status et vérifier que git n'indique plus de fichier à modifier.

Questions : 
Quelle est la différence entre git add et git commit ? 
Git stocke-t-il l'entiereté de chaque fichier à chaque commit ou est-il un peu plus intelligent ? 

### 2. Enlever un fichier qui s'apprête à être commit

1. Sur la même branche créer deux fichier nommés test1.py et test2.py
2. Ajouter les deux fichiers au staging avec git add (ne pas les commit)
3. Vous vous rendez compte que vous ne voulez pas commiter test2.py 
   A l'aide de git reset HEAD nom_ficher enlever test2.py du stagging
4. commit test1.py avec le message que vous voulez

### 3 Branches

1. Créer une branche nommée "seconde-branche" avec la commande git checkout -b "nomdelabrancheacreer"
2. Afficher toutes les branches avec la commande git branch
3. créer un fichier "fichier2.txt" et mettre une phrase simple dedans
4. avec git add et git commit sauvegarder le fichier dans git.
5. retourner sur l'autre branche avec la commande git checkout "nomdebranch"
6. Le fichier fichier2.txt a disparu ! Est-ce normal ?
7. Avec la commande git merge fusionner le commit de la branche "seconde-branche" dans la première branche

### 4. Ignorer des fichiers et dossier.

1. créer un dossier data et y ajouter un fichier data.txt dedans
2. faire un git status
3. créer un fichier .gitignore 
4. ajouter une ligne qui contiendra "data/"
5. refaire un git status. Normalement le fichier n'apparait plus en rouge : il est désormais ignoré par git.
