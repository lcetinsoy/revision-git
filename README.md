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

### 2 Branches
0. faire un fork du repo
1. Créer une branche avec votre prenom/username
2. Ajouter un fichier le commiter et pusher sur la branche

### 3. Enlever un fichier qui s'apprête à être commit

1. Sur la même branche créer deux fichier nommés test1.py et test2.py
2. Ajouter les deux fichiers au staging avec git add (ne pas les commit)
3. Vous vous rendez compte que vous ne voulez pas commiter test2.py 
   A l'aide de git reset HEAD nom_ficher enlever test2.py du stagging
4. commit test1.py avec le message que vous voulez


### 4. ignore des fichiers et dossier.

créer un dossier data
faire un git status
créer un fichier .gitignore 
et mettre data/ dedans
refaire un git status et assurez vous que git 
considère plus le fichier
