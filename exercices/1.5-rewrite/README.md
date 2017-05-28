Ré-écrire l'histoire
====================

Objectifs
---------
- Savoir modifier un commit (commentaire et contenu).
- Comprendre l'impact de la modification d'un commit sur l'arbre.
- Savoir réordonner ses commit, les fusionner et les splitter.

Les Commandes
-------------
- *git commit --amend*
- *git rebase --interactive*


### Exercices ###
Utiliser le dépôt my-vertx-first-app et se mettre sur la branche *wip-1*. 
- Afin de conserver l'état initial, créer un tag *wip-old-1*.
- Commencer par consulter l'historique pour comprendre ce que fait cette branche.

L'historique de cette branche est confus, nous allons le re-travailler.

#### Re-travailler l'historique ####
1. Les urls ajoutées par le dernier commit ("/api/beer") sont inconsistentes avec les précédentes ("/api/whiskies").
  - modifier le dernier commit pour que les urls "/api/beer" aient la forme "api/beers".
  - changer le commentaire en ;
   > - change routes for whiskies
   > - add routes for beers 
  - constater l'impact sur le graphe d'historique
  - "sauvegarder" l'état actuel avec un tag *wip-old-2*

2. Les 4 premiers commit de la branche consistuent en réalité une modification unique. 
 - fusionner ces 4 commits pour en faire un unique "Add a Beer class"
 - constater l'impact sur le graphe d'historique
 - "sauvegarder" l'état actuel avec un tag *wip-old-3*

3. On a maintenant 2 commits mais on voudrait en inverser l'ordre
 - inverser l'ordre de ces 2 commits
 - constater l'impact sur le graphe d'historique
 - "sauvegarder" l'état actuel avec un tag *wip-old-4*

4. Le 1er commit de la branche est en fait constitué de 2 modifications : "add routes for beers" et "change routes for whiskies"
 - splitter ce commit pour avoir 1 commit pour chacun de ces changement
 - constater l'impact sur le graphe d'historique
