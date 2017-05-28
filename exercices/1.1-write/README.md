Créer et faire évoluer un dépôt
===============================

Objectifs
---------
- Savoir ajouter de nouveaux commit.
- Comprendre le mécanisme d'indexation derrière un commit.

Les Commandes
-------------
- *git init*
- *git status*
- *git add [--patch]* et *git rm*
- *git commit*
- *git diff [--cached]*

### Exercices ###

#### Création de dépôt ####
Créer un nouveau dépôt "my-first-repo"

#### Écriture de commit ####
Faire le commit initial avec un ficher hello-word.txt
  - écrire le ficher ("Hello world!" fera l'affaire)
  - consulter le statut du dépôt
  - ajouter le fichier à l'index
  - Une fois satisfait du contenu et que celui-ci est indexé, figé l'index dans un commit avec comme commentaire : "initial commit : Hello World"

On peut aussi choisir le nom et l'email qui apparaissent dans les commit en changeant les config user.name et user.email

#### Écriture de commit partiel ####
Le fichier [top-dire-bonjour-enervante.md](https://bitbucket.org/gobinax/lacombe-formation/raw/175a455b6bab17db0f522d89750bd33429c98d13/repositories/top-dire-bonjour-enervante.md) contient un top 5 des manières énervant de dire bonjour au bureau. On souhaite ajouter le contenu au fichier hello-word mais en faisant plusieurs commit.
> * c8da297 (HEAD -> master) top 3 -> top 5 des hello
> * c405c14 top 3 des hello

1. copier le fichier *top-dire-bonjour-enervante.md* dans le dépôt. Comme nous ne souhaitons pas avoir ce ficher dans l'index, on va l'ajouter à un répertoire *temp/* que l'on va ignorer.
  - créer un répertoire *temp/*
  - l'ajouter à la liste des fichiers ignorés
  - commit de cette liste
2. ajouter le contenu de *top-dire-bonjour-enervante.md* à hello-world.txt
3. ajout des 3 premiers hello à l'index puis
  - vérification de l'index
  - commit
4. ajout des 2 suivants à l'index puis
  - vérification de l'index
  - commit
