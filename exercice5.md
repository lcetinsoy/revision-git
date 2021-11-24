# Github jobs (github actions)

Il est possible de demander à github de lancer des scripts (des actions)
à chaque fois que quelqu'un fait un push sur une branche. 

Cela permet notament de : 
- vérifier la qualité du code avant d'accepter un merge
- vérifier que le logiciel passe des tests automatique
- et si c'est le cas, potentiellement initier un déploiement automatique avec l'outil de votre choix (comme ansible, création d'image et push sur un registry, etc.)


Exercice 1

1. Créer un repository sur github vierge 
2. cloner le repository en local 
3. Créer une branch test-action
4. Créer un dossier .github/workflows
5. créer un fichier yaml nommé github-actions-demo.yml avec le contenu suivant

(cf  : https://docs.github.com/en/actions/quickstart)

```yaml

name: GitHub Actions Demo
on: [push]
jobs:
  Explore-GitHub-Actions:
    runs-on: ubuntu-latest
    steps:
      - run: echo "🎉 The job was automatically triggered by a ${{ github.event_name }} event."
      - run: echo "🐧 This job is now running on a ${{ runner.os }} server hosted by GitHub!"
      - run: echo "🔎 The name of your branch is ${{ github.ref }} and your repository is ${{ github.repository }}."

```

6. Ajouter et commiter le dossier et le fichier yml
7. Push la branche test-actions
8. Aller sur l'interface github et vérifier qu'un job s'est lancé et voir ce qu'il se passe. 


Exercice 2 

1. On veut maintenant executer un script python simple  (job.py) fourni
ajouter le fichier job.py dans le dossier du workflow et modifier le fichier yaml pour qu'il lance le fichier python


Exercice - pour les real professionals

On veut build une image docker et la push sur le registry dockerhub 

- Reprendre le fichier app.py qui permet de créer un webservice
- Reprendre le fichier dockerfile qui permet de build une image
- Créer un script bash qui installe docker et build l'image et qui affiche docker images
- Modifier le fichier fichier yaml pour que cela lance le script
- push la branche et vérifier bien que le job afficher bien votre image bien build
- Modifier le script bash pour que désormais ça fasse un docker tag, un docker login et un docker push pour push votre image sur votre registry

Exercice 3 : bonus

En vrai pour faire ce genre de chose on va plutôt utiliser des actions déjà crée par d'autres 

par exemple cette action https://github.com/docker/build-push-action permet de spécifier une image à créer à partir d'un dockerfile situé à la racine du projet, de le build et de push l'image correspondante sur le registry.

Reprendre l'exercice 2 et faire en sorte que votre action utilise l'action proposée dans le lien ci dessus et non pas un script bash 
