---
layout: post
title: Git Style Guide
description: Buenas prácticas a la hora de usar git / git-flow
date: 2022-03-09 23:12:00 -0500
categories: dev
---
# {{ page.title }}

![workflow](/assets/git-style-guide-workflow.png)

- Las ramas ***feature*** y ***release*** se crean a partir de ***develop***. Mientras que ***hotfix*** se crea de ***master***.
- ***Hotfix***  y ***release*** son mergeados en ***master*** y ***develop***.
- ***Feature*** es mergeado en ***develop***.

## Branches

Usar nombres cortos y descriptivos para las ramas, si se usara mas de una palabra usar nomenclatura CamelCase.

``` sh
# Master
$ git checkout -b master

# Develop
$ git checkout -b develop

# Features
$ git checkout -b feature/myFeature

# Releases
$ git checkout -b release/vX.X.X

# Hotfixes
$ git checkout -b hotfix/myFix
```

## Commits

Cada commit debe estar compuesto por un solo cambio *lógico*. Por ejemplo, si un cambio corrige un error y, a la vez, optimiza el rendimiento de un aspecto de la aplicación, debes separarlo en dos commits.

El commit debe estar en modo imperativo, empezar con mayúscula y tener menos de 50 caracteres.

``` sh
$ git commit -m "--" ❌
$ git commit -m "Implement session expiration"
```

## Tags

Cada commit que contenga el proyecto listo para producción debe llevar un tag con su versión actual.

``` sh
$ git tag vX.X.X -m "vX.X.X"
```

*Si tienes alguna duda con respecto al tema, por favor, envíame un mensaje!*