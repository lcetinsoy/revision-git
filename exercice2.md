# A plusieurs

1. Mettez vous par deux
2. L'un des membre du groupe (personne A) crée un repository sur github
3. A invite B au à liste des contributeurs du repo sur github (dans paramètres)
4. A crée un fichier et l'ajoute dans le repository
5. A commit et push. 

Une fois que c'est fait 

B clone le repository puis modifie le fichier créé par A. 
B commit et push 

Pendant ce temps A modifie le fichier qu'il a créé, 
le commit (sans le push). 

Quand B a push, A tente de push et devrait avoir une erreur. 

A suit les indications de l'erreur et un conflit devrait être apparu ! 

## Résoudre un conflit

Quand un même ficher est modifié par deux personnes différents, git ne sait pas
(sauf dans certains cas) quels modifications garder. 

A ouvre le fichier ayant le conflit. Discuter à deux quelle modification garder

A modifie le fichier en conséquence

A add le fichier modifié au staging, le commit 

A peut désormais pusher


