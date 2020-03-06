Explorer l'historique
=====================

Objectifs
---------
- Savoir explorer un historique/arbre de dépôt git.
- Savoir visualiser le contenu d'un commit.

Les Commandes
-------------
- *git log*
- *git show*
- *git diff*
- *git merbe-base*

### Exercices ###
Utiliser le dépôt - [my-vertx-first-app](https://github.com/gobinax/git-formation/raw/master/repositories/my-vertx-first-app.zip)

#### Visualiser un ensemble de commits ####
1. Afficher l'historique
2. Afficher l'historique sous une forme plus compact
3. Afficher l'historique complet (pas seulement celui de la branche en courante)
4. Afficher l'historique complet sous forme de graphe
5. Afficher uniquement l'historique des branches *master* et *post-3*
6. Configurer l'alias *git l* pour qu'il effectue la commande suivante :
> git log --graph --decorate --pretty=oneline --abbrev-commit

7. Utiliser la nouvelle commande *git l* pour
  - voir le graph complet
  - voir le graphe des branches *post-2* et *post-3*

#### Visualiser le contenu d'un commit ####
1. Afficher la modification apportée par le dernier commit
2. Afficher la modification apportée par l'avant dernier commit
3. Afficher la modification apportée par le dernier commit de la branche post-2
4. Afficher la modification apportée par l'avant dernier commit de la branche post-2
5. Afficher la modification apportée par le commit avec le commenatire "Migrate to vert.x 3.1"
6. Afficher les modification apportée à post-3 depuis la dernière fois qu'elle a été fusionnée avec master
