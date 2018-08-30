# A plusieurs

1. Mettez vous par deux
2. L'un des membre du groupe (personne A) crée un repository sur github
3. A invite B au à liste des contributeurs du repo sur github (dans paramètres)
4. A crée un fichier et l'ajoute dans le repository

Une fois que c'est fait 

B clone le repository puis 
modifie le fichier créé par A. A commit et push. 

Pendant ce temps A le fichier qu'il a créé et le commit
le commit (sans le push). 

Quand B a push, A tente de push et devrait avoir une erreur. 

A suit les indications de l'erreur et un conflit devrait être apparu ! 

## Résoudre un conflit

Quand un même ficher est modifié par deux personnes différents, git ne sait pas
(sauf dans certains cas) quels modifications garder. 

Ouvrir (A) le fichier ayant un conflit et l'analyser. 

Puis décider quel partie garder et le modifier

avec git add ajouter le fichier au stage, faire un commit 

puis il doit être possible de push désormais.


