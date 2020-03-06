Naviguer dans l'historique des versions
=======================================

Objectifs
---------
- Savoir changer de branche en cours.
- Savoir modifier la branche en cours.
- Savoir retrouver des commit "perdus".

Les Commandes
-------------
- *git checkout*
- *git reset*
- *git reflog* et *git log --walk-reflogs*

### Exercices ###
Utiliser le dépôt my-vertx-first-app.

#### Changer de branche ####
1. Questions :
  - Quelle est la version en cours ?
  - Comment s'appelle la référence vers la version en cours ?
2. Changer de version en cours : passer sur la branche post-3

#### Travail détaché ####
Le travail effectué sur la branche *post-3* depuis le dernier merge dans master ne nous convient pas.

1. Noter le hash de la version actuelle : bbc529b
2. Noter le hash de la version de *post-3* avant le dernier merge dans master : eb2c7fcq
3. Faire pointer la version en cours sur ce commit puis :
  - Vérifier l'historique de la version courante et de la branche *post-3*
  - Vérifier le statut.
4. Supprimer le fichier *LICENSE* puis :
  - La versionner dans un nouveau commit.
  - Vérifier à nouveau l'historique de la version courante et de la branche *post-3*.
  - Noter le hash de la version courante
  - Expliquer la situation.
5. Se réattacher à la branche *post-3*

#### Changer la branche ####
1. Tout en restant sur la branche *post-3*, on souhaire revenir à la version précédente (celle où l'on a supprimé le fichier *LICENSE*)
  - Faire pointer la branche *post-3* sur cette version
  - Vérifier l'état de l'index. S'assurer que l'index et le working tree correspondent.
2. Finalement on veut restaurer le fichier *LICENSE*
  - Faire revenir la branche *post-3* 1 commit en arrière. N'utiliser qu'une seule commande. Le working tree et l'index doivent correspondre.

#### Retrouver les commits perdus ####
1. Finalement, on souhaite faire *post-3* à son état initial
  - utiliser l'audit de git : le reflog
  - retrouver le hash de la version initial de *post-3* (on peut vérifier que c'est le commit qui nous intéresse avec un *git l post-3 <hash>)
  - ramener la branche *post-3* à cette version
