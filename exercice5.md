# Github jobs (github actions)

Il est possible de demander à github de lancer des tâches (des actions)
à chaque fois que quelqu'un fait un push sur une branche. 

C'est un mécanisme de Pipeline proposé par Github qui s'appelle github Action. 

Cela permet notament de : 
- vérifier la qualité du code avant d'accepter un merge
- vérifier que le logiciel passe des tests automatique
- et si c'est le cas, potentiellement initier un déploiement automatique avec l'outil de votre choix (comme ansible, création d'image et push sur un registry, etc.)

Pour cela il faut créer un fichier de configuration au format yaml à placer dans un sous dossier spécifique : workflows lui même situé dans un dossier .github à la racine du projet. C'est à vous de créer ces dossiers.

Exercice 1

1. Créer un repository sur github vierge 
2. cloner le repository en local 
3. Ajouter un fichier et le commit
5. Créer un dossier .github/workflows
6. créer un fichier yaml nommé github-actions-demo.yml avec le contenu suivant

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
7. Faire un push de votre branche main
8. Aller sur l'interface github, dans l'onglet "Actions" (à coté de Pull request). Vérifier que l'action s'est déclenchée et que les commandes "echos" ont bien démarrées. 


Exercice 2 

On veut maintenant utiliser github action afin d'executer un script python simple 

1. A la racine de votre projet, créer un fichier python job.py qui contient

```python
a = 2
print("coucou", a)
```

2. Modifier le fichier yaml pour qu'il lance le fichier python

Si vous essayer de faire un push, vous vous rendrez compte que l'action échoue. En effet, 
par défaut, github Action, ne récupère pas le code du repository avant de lancer l'action. 

Pour que github action récupére les fichiers du repository git il faut modifier le fichier yaml 
et ajouter la section suivante 

```
  - uses: actions/checkout@v4
```
Vous pouvez vous référer à https://docs.github.com/en/actions/quickstart pour cela


2. Récupérer ou faire une fonction qui calcule la moyenne des valeurs d'une liste. Faire un test unitaire avec pytest test et l'ajouter dans le repository. 
3. Faire en sorte que les tests unitaires soient lancés dans le CI/CD à chaque push. 
4. Comparer ce qu'il passe quand la fonction est bugguée et que les tests ne passent pas et quand la fonction marche correctement
