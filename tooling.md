Le Tooling
==========

## Ligne de commande ##

La ligne de commande est le meilleure des outils pour git. Créé par Linus Torvalds,
on est dans l'esprit de Linux avec beaucoup de petites commandes composables. Être à l'aise avec est donc indispensable si on veut tirer profit de git.

Pour être productif, on va quand même devoir "pimper" un peu cette ligne de commande.

#### Linux/OSX ####

##### bash completion #####
[bash-completion](https://github.com/scop/bash-completion) est un ensemble de scripts disponibles pour bash. Il s'installe par package (apt-get sous debian, brew sous OSX).

Pour git, il va nous permette de booster la completion et de faire un *git commit* en ne tapant que *git com \[tab\]*

##### git ps1 #####
Quand on travail en ligne de commande, un bon prompt c'est important. À titre d'exemple, voici le mien :
```
[\[\e[0;32m\]\u\[\e[0m\]] \[\e[0;36m\]\w\[\e[0m\]\[\e[0;33m\] $(__git_ps1)\[\e[0m\]\n\[\e[0;33m\]$\[\e[0m\]
```

La partie importante est ```$(__git_ps1)```

Pour tester si cette function est dispo, on peut taper ceci ```echo $(__git_ps1)```. La fonction affiche la branche si on est dans un dépôt git et rien sinon.

Les post suivants sur stackoverflow peuvent aider en cas de problème sur [Ubuntu](https://stackoverflow.com/questions/9717137/displaying-git-branch-name-in-prompt-does-not-work-in-screen) or
[OSX](https://stackoverflow.com/questions/12870928/mac-bash-git-ps1-command-not-found).

#### Windows ####
La ligne de commande sous Windows, ce n'est pas ce qu'il se fait de mieux. Heureusement, [git-for-windows](https://git-for-windows.github.io/) est là pour nous aider en nous fournissant un terminal (presque) à la auteur d'un bash sous Linux/OSX.

## GUI ##
La ligne de commande est très puissante, mais certaines opérations comme la visualisation d'un gros commit où un merge "velu" seront plus facile et comfortable avec un bon outil graphique.

##### Git Kraken #####
https://www.gitkraken.com/

Multi-plateforme, joli et ergonomique, c'est un bon outil graphique.

##### IntelliJ IDEA #####
Si on travaille sur cet IDEA, pas la peine de compléter avec un autre outil graphique. IDEA fait très bien le job.
