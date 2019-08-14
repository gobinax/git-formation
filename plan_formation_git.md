# Formation Git

## Matinée

### Introduction

Début, tour de table :

* présentation
* attentes
* où vous situez-vous (1-5) ?
  * pourquoi ?
    1. je me sens dépassé / je sais faire le minimum
    2. j'ai souvent besoin de me faire aider et je me sens dépassé
    3. j'arrive à mes fins sans toujours comprendre, ni être optimal
    4. j'ai pas besoin d'aide, j'ai encore des choses à apprendre
    5. je vois pas ce que je pourrais apprendre de plus
* aucune questions stupides, si vous ne dites pas que vous ne savez pas, vous n'apprendrez pas, n'hésitez pas à demander tant que vous n'avez pas compris

### CI / CD

Présentation CI / CD, cycle de vide de l'application

[~CI](https://landscape.cncf.io/category=continuous-integration-delivery&format=card-mode&grouping=category)

[~CD](https://landscape.cncf.io/category=automation-configuration&format=card-mode&grouping=category)

1. Code - Source
2. Build - Livrable
3. Deploy - Env
4. Run - Valeur
    * Monitoring
    * Alerting

#### Démo

GitLab CI

```python
def hello(name):
    return "Hello " + name

def test_hello_world():
    assert hello('world') == 'Hello world'
```

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

1. créer le repo
2. lancer la CI
3. montrer que la CI fonctionne
4. télécharger le fichier
5. ajouter un test qui fail
6. montrer que la CI fail
7. montrer que le fichier téléchargé est resté sur la version précédente
8. corriger le test et reprendre à l'étape 3

---

pause

---

### Questions ?

### Présentation théorique de git

#### Historique

* Créé par Linus Torvald en 2005
* Système de gestion décentralisé
* Successeur de SVN
* Concurrent de Mercurial

#### Slide

* commit message :

> tell me what the software does (not what you did)

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

### Retro

* vos attentes ?
* encore des questions / revenir sur des points ?
* où pensez-vous vous situer ? (1-5)

### Aller plus loin

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
