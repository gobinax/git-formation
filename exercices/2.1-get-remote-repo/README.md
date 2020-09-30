Obtenir un dépôt distant
========================

Objectifs
---------
- Créer un dépôt en tant que clone de dépôt distant
- Savoir obtenir les informations de dépôt distant de son dépôt
- Comprendre l'aspect décentraliser de git

Les Commandes
-------------
- *git clone*
- *git remote*


### Exercices ###
Faire une copie propre du dépôt *my-vertx-first-app* et la nommer *repo-origin*.

#### Clonage de dépôt ####
1. Faire un clone de *repo-origin* que l'on nomme *repo-clone*.
2. Comparons les 2 dépôts :
  - Comparer les historiques (graphe complet)
  - Comparer les branches.
  - Expliquer pourquoi les 2 dépôts n'ont pas les mêmes branches.
  - Expliquer la différence entre une copie de dépôt et un clonage.
3. Dans *repo-clone*, la branche *post-1* n'existe pas.
  - Faire une *git checkout post-1*.
  - Expliquer le résultat.
  - Expliquer la différence en entre *git checkout post-1* et *git checkout origin/post-1*
#### Le dépôt distant ####
4. Faire *git remote*, puis un *git remote -v*.
  - À quoi servent ces commandes ?
5. Faire un *git remote remove origin*
  - Expliquer ce que fait la commande.
6. Faire un *git remote add origin repo-origin*
  - Lister les branches et consulter leur historique. Où sont passées les *origin/post-1*, *origin/post-2* ... ?
