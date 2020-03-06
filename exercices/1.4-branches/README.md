Vie et mort des branches
========================

Objectifs
---------
- Savoir créer une nouvelle branche.
- Savoir changer l'origine d'une branche.
- Savoir fusionner des branches.
- Comprendre la différence entre une fusion de rattrapage et une ré-integration.
- Savoir mettre de côté un travail en cours.

Les Commandes
-------------
- *git branch* et *git checkout -b*
- *git merge [--no-ff]*
- *git rebase*
- *git cherry-pick*
- *git stash*

### Exercices ###
Utiliser le dépôt my-vertx-first-app (reprendre l'original en cas de modification).

#### Démarrer une nouvelle branche ####
1. On veut supprimer les fichier *LICENSE* et *README.md*
  - Démarrer une nouvelle branche "remove-license" en partant eb2c7fc (ancêtre commun de post-3 et master).
  - supprimer le fichier *LICENSE* et versioner avec un commit
  - faire de même avec *README.md*

#### Changer l'origine d'une branche ####
1. Finalement, on préfère faire partir cette branche de master
  - changer l'origine de la branche pour qu'elle parte de master

#### Picorer un commit ####
1. On préfère avoir chacun de ces changement dans une branche
  - Démarrer une nouvelle branche "remove-readme" en partant de master.
  - récupérer le commit de suppression de *README.md*

#### Ré-intégrer une branche ####
1. Ré-intégrer la branche *remove-readme* dans *master*
  - faire une merge de *remove-readme* dans *master*
  - supprimer la branche *remove-readme*
2. Ré-intégrer la branche *remove-license* dans *master*
  - Changer l'origin de *remove-license*. La refaire partir de *master*
  - faire une merge de *remove-license* dans *master* sans fast-forward
  - supprimer la branche *remove-license*
  - comparer l'historique et les 2 méthodes de merge

#### Régler les conflits ####
1. Ré-intégrer les branches *refacto-1* et *refacto-2* dans *master* 
  - ne pas faire de rebase avant le 2ème merge
  - un conflit apparait lors du merge : abandonner le merge en cours.
  - merger à nouveau, cette fois en resolvant le conflit.
2. Ré-intégrer les branches *refacto-1* et *refacto-2* dans *master*. sans faire de rebase
  - faire un rebase avant le 2ème merge
  - abandonner le rebase en cours
  - refaire le rebase cette fois en resolvant le conflit
3. Comparer les 2 méthodes

#### Mettre de côté ####
1. Commencer à éditer un fichier. 
  - Le mettre de côté avec *git stash*.
  - Visualiser l'arbre.
  - Comparer cette technique avec une utilisation de branche temporaire
  

