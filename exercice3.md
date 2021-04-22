# Retour sur les branches

Dans le premier exercice on a vu les branches : vous avez créé une branche
et fait des modifications dessus. 

1. Retourner dans le repository où vous avez créé la branche. 
lister les fichiers avec dir ou ls

2. Avec la commande git checkout retournez la branche master 
et vérifier que le fichier que vous aviez ajouter sur votre branche
n'existe plus

# Merge

En général on crée des branches pour ne pas faire de modification
directe sur la branche master qui est utilisée pour les déploiement

Mais quand on est content d'une modification effectuée sur une branche
on veut la fusionner dans master. 

1. Se mettre dans la branche master
2. Fusionner la branche où vous aviez fait les modifications dans master
   a l'aide la de git merge 
   
3. Vérifier que les modifications sont bien intégrées dans master
4. Push vers le repository distant
5. Lire https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Rebaser-Rebasing

