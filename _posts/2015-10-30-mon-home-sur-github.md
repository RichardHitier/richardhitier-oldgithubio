---
layout: post
title: "mon home sur github"
description: ""
category: 
tags: []
---
{% include JB/setup %}

$home sweet $home, ou comment être vraiment chez moi partout
où je vais.

# dépôt github

tout ce qui est indispensable est donc stocké sur le github

# mise à jour
dès après la création de l'utilisateur sur le noueveau pc,
je clone le git, masi dans un répertoire existant.
donc

```
$ sudo $(package-mgr) vim, zsh, screen
```
puis

```
$ git init
$ git remote set-url origin https://github.com/RichardHitier/home.git
$ git branch --set-upstream-to=origin/master master
$ git pull 
```
et rulez

# mise à jour (2)
ah  non, argh, ya des trucs qui manquent encore 

``` 
$ git submodule init
$ git submodule update
```


# dernières mises au point

à automatiser ?

```
$ sudo $(package-mgr) vim, zsh, screen
$ chsh -s zsh
```

et rulez \o/


# pointeurs

https://help.github.com/articles/changing-a-remote-s-url/

