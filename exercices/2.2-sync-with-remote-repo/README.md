Se synchroniser avec un dépôt distant
=====================================

Objectifs
---------
- Savoir mettre à jour son dépôt avec le dépôt distant
- Savoir envoyer des modification vers le dépôt distant
- Comprendre le mécanisme de branche "remote"

Les Commandes
-------------
- *git fetch*
- *git pull*
- *git push [--set-upstream]*
- *git branch [--set-upstream-to|--unset-upstream]*

### Exercices ###
On reprend là où on a laissé l'exercice précédent.

#### Les branches distantes ####
1. Récupérer les branches distantes.
  - Quelle différence entre *git fetch* et *git pull*.

2. On travaille sur *post-1*
  - Ajouter un commit quelconque sur cette branche dans *repo-origin*.
  - Dans *repo-clone*, mettre à jour *origin/post-1* sans mettre à jour *post-1*.
  - Mettre à jour *post-1*.
  - Revenir en arrière sur *post-1* puis ajouter un commit. Les branches *origin/post-1* et *post-1*
  sont maintenant divergentes. Faire un *git pull* et observer l'arbre des commits.
  - Recommencer mais avec la commande *git pull --rebase*
  - Mettre à jour le dépôt distant avec les commits de *post-1*.

3. Créer une nouvelle branche
  - Faire 1/plusieurs commit.
  - "Pusher" cette branche sur le dépôt distant.
