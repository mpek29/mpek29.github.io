---
layout: page
title: Python 3
importance: 1
---

## Notion de variable
La notion de variable désigne un conteneur ayant pour but de stocker une **valeur** sous forme de donnée ayant une **adresse mémoire** propre.

## Les principaux types de données
Les **valeurs** énoncées dans la partie précédente sont d'un type précis, ici on décrire les principaux types de données.

| **Catégories de données**  | **Types de données**        |
|--------------------------  |---------------------------  |
| Type de texte              | `str`                       |
| Types numériques           | `int`, `float`, `complex`   |
| Types de séquence          | `list`, `tuple`, `range`    |
| Type de mappage            | `dict`                      |
| Type booléen               | `bool`                      |

<br>

## Opérateurs
Il est possible de faire interagir les variables entre elles à l'aide d'opérateurs afin de générer des valeurs de type `bool` (qui pourront être par la suite utilisé pour faire usage d'instruction conditionnelle ou d'instruction de boucle de la forme `while`).

| **Différents opérateurs**   | **Types de données**              |
|---------------------------  |---------------------------------- |
| Opérateurs de comparaison   | `==`, `!=`, `>`, `<`, `>=`, `<=`  |
| Opérateurs logiques         | `and`, `or`, `not`                |
| Opérateurs d'appartenance   | `in`, `not in`                    |

<br>

## `if` Instruction conditionnelle
Une instruction conditionnelle est une instruction (appel de fonction, affectation de variable, etc.) qui sera ignorée ou considérée en fonction de la valeur du booléen placé à la suite du mot "if". Si ce booléen vaut True, l'instruction sera considérée et si ce booléen vaut False, l'instruction sera ignorée.

``` python
if True :
  print('Ceci sera affiché')
else:
  print('Ceci ne sera pas affiché')
```

``` python
if False :
  print('Ceci ne sera pas affiché')
else:
  print('Ceci sera affiché')
```


## Instructions de boucle
### `while`
Une instruction de boucle de la forme `while` est très proche d'une instruction conditionnelle mis à part qu'au lieu de simplement ignorer ou considérer une instruction, on va répéter en boucle l'instruction temps que la valeur du booléen n'est pas False.

``` python
while True :
  print('Ceci sera répété en boucle')
```

``` python
while False :
  print('Ceci ne sera pas répété en boucle')
```


### `for`
Une instruction de boucle de la forme `for` permet essentiellement de parcourir une séquence (cela correspond à 3 types comme vu précédemment : `list`, `tuple` et `range`).

On peut parcourir ainsi une liste de façon on ne peut plus classique.
``` python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
  print(x)
```

On peut incrémenter une valeur au fur et à mesure des répétitions d'un boucle grace à range().
``` python
for x in range(2, 6):
  print(x)
```

Cela peut nous amener à une alternative de la première boucle permettant de garder en note l'indice de l'éléments courant.
``` python
fruits = ["apple", "banana", "cherry"]
for i in range(len(fruits)):
  fruit = fruits[i]
  print(fruit)
```


## Source
- <https://www.w3schools.com/python/python_reference.asp>