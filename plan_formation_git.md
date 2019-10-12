# Formation Git

## Matinée

### Introduction

Début, tour de table :

* présentation
* attentes
* où vous situez-vous (1-5) ?
  * pourquoi ?
  * [Niveaux](./niveaux.md)
* comment l'utilisez-vous (CLI / GUI (lesquelles)) ?
* aucune questions stupides, si vous ne dites pas que vous ne savez pas, vous n'apprendrez pas, n'hésitez pas à demander tant que vous n'avez pas compris

### Du code à la prod : Présentation cycle de vie de l'application

Faire deviner les différentes étapes du cycle de vie de l'application, entre le moment où on écrit une ligne de code et le moment où ça apporte de la valeur

Expliquer le role de chaque étapes

Préciser que ce **n'est qu'une** façon de voir ce cycle

1. Code - Source
2. Build - Livrable (Continuous Integration + Continuous Delivery)
3. Deploy - Env (Continuous Deployment)
4. Run - Valeur
    * Monitoring
    * Alerting

Faire deviner des outils permettant de réaliser ces étapes

Liste non exaustive d'outils permettant de gérer la :

* [Continuous Integration](https://landscape.cncf.io/category=continuous-integration-delivery&format=card-mode&grouping=category)
* [Continuous Deployment](https://landscape.cncf.io/category=automation-configuration&format=card-mode&grouping=category)

#### CD != CD

Deux définitions de CD : Continuous Delivery VS Continuous Deployment

#### Démo GitLab CI

`hello.py`

```python
def hello(name):
    return "Hello " + name

def test_hello_world():
    assert hello('world') == 'Hello world'
```

`.gitlab-ci.yml`

```yaml
stages:
    - test
    - deploy

image: python:3-alpine

test:
    stage: test
    script:
        - pip3 install pytest
        - pytest hello.py

pages:
    stage: deploy
    script:
        - mkdir public
        - mv hello.py public/
    artifacts:
        paths:
            - public/
        expire_in: 1 week
```

1. créer le repo local

   ```sh
    git init
    git add .
    git commit
    ```

2. créer le repo [sur GitLab](https://gitlab.com/projects/new) et ajouter la remote

    ```sh
    git remote add origin git@gitlab.com:USER/REPO.git
    ```

3. lancer la CI `git push origin master`
4. montrer que la CI fonctionne
5. télécharger le fichier
    `https://USER.gitlab.io/REPO/hello.py`
6. ajouter un test qui fail
7. montrer que la CI fail
8. montrer que le fichier téléchargé est resté sur la version précédente
9. corriger le test et reprendre à l'étape 3

---

pause

---

### Questions ?

### Présentation théorique de git

#### Historique

* Créé par Linus Torvald en 2005
* Système de gestion de versions décentralisé
* Successeur de SVN
* Concurrent de Mercurial
* Git != GitHub & GitLab & BitBucket ...

#### Slide

* commit message :

> tell me what the software does (not what you did)

jusqu'à la définition d'un commit

#### Frise des espaces

Initialisation de la [frise montrant les commandes permettant de passer d'un espace à l'autre](http://www.ndpsoftware.com/git-cheatsheet.html)

Durant toute la journée, chaque nouvelles commandes découvertes est ajoutées sur la "frise des espaces"

### Exo

[Write](https://github.com/gobinax/git-formation/tree/master/exercices/1.1-write)

#### Slide

jusqu'à HEAD / Branche / Tag

### Exo

Si on a le temps

[Explore](https://github.com/gobinax/git-formation/tree/master/exercices/1.2-explore)

---

pause déjeuner

---

## Après midi

### Questions ?

### Exo

Si pas fait avant manger

[Explore](https://github.com/gobinax/git-formation/tree/master/exercices/1.2-explore)

### Slide

* checkout
* reset

### Exo

[Navigate](https://github.com/gobinax/git-formation/tree/master/exercices/1.3-navigate)

---

pause

---

### Questions ?

### Slide

* merge
* rebase

### Exo

[Branches](https://github.com/gobinax/git-formation/tree/master/exercices/1.4-branches)

---

pause

---

### Questions ?

### Slide

* remote

### Aller plus loin

* compléter la frise des espaces
* Démo rebase interactive
  * pick
  * reword
  * reorder
  * drop
  * squash
* Démo remote repo
  * fetch
  * push
  * pull

### Retro

Fin, tour de table

* vos attentes ont elles étaient atteintes ?
* encore des questions / revenir sur des points ?
* où pensez-vous vous situer ? (1-5)

ROTI de la journée
