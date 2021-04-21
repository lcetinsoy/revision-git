# revision-git

Quelques exercices 


## Exercices

### 1 Basics

1. Cloner le repository avec la commande git clone
2. Créer un fichier dont le nom est votre prénom ou username
3. lancer la commande git status. Lire le message.
4. avec git add ajouter le fichier pour qu'il soit ajouté dans le prochain commit.
5. faire un git status. Qu'est ce qui a changé ? 
6. valider la sauvegarde du commit avec la commande git commit. Faire en sorte que le message du commit soit   "mon premier commit"
7. Faire un git log pour vérifier que le commit a bien été ajouté à l'historique des commits

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

### 4. ignore des fichiers et dossier.

créer un dossier data
faire un git status
créer un fichier .gitignore 
et mettre data/ dedans
refaire un git status et assurez vous que git 
considère plus le fichier
