# Les conflits à plusieurs

1. Mettez vous par deux
2. L'un des membre du groupe (personne A) crée un repository sur github
3. A invite B à la liste des contributeurs du repo sur github (dans paramètres)
4. A crée un fichier et l'ajoute dans le repository
5. A commit et push. 

Une fois que c'est fait 

6. B clone le repository puis modifie le fichier créé par A. 
7. B commit et push 

8. Pendant ce temps A modifie le fichier qu'il a créé et le commit **sans le push** 


9. Quand B a push, A tente de push et devrait avoir une erreur. 

10. A suit les indications de l'erreur et un conflit devrait être apparu ! 

## Résoudre un conflit

Quand un même ficher est modifié par deux personnes différents, git ne sait pas
(sauf dans certains cas) quels modifications garder. 

1. A ouvre le fichier ayant le conflit. Discuter à deux quelle modification garder

2. A modifie le fichier en conséquence

3. A add le fichier modifié au staging, le commit 

4.A peut désormais pusher

Refaire les deux séries d'exos en inversant les roles
