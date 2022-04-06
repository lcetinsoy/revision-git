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
7. Push la branche test-actions
8. Aller sur l'interface github et vérifier qu'un job s'est lancé et voir ce qu'il se passe. 

Exercice 2 

On veut maintenant executer un script python simple 

1. Créer un fichier python job.py qui contient

```python
a = 2
print("coucou", a)
```

Ajouter le  fichier job.py à la racine du projet et modifier le fichier yaml pour qu'il lance le fichier python

Il faudra ajouter dans la section step la ligne suivante : 

```
  - uses: actions/checkout@v2
```

Ce morceau de code va permettre de récupérer le code du projet dans l'environnement d'execution. 

2. récupérer le code qui calcule la moyenne des valeurs et le test que vous avez fait. Ajouter les fichiers dans votre projet et faire en sorte que les tests unitaires soient lancés dans le CI/CD à chaque push. Comparer ce qu'il passe quand la fonction est bugguée et que les tests ne passent pas et quand la fonction marche correctement
