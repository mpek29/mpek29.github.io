---
layout: page
title: Système d’ouverture de coffre
description: Machine à état numérique
img: assets/img/projects/safe_opening_system/main.jpg
importance: 1
category: Elec. num
---

# Cahier des charges

Le système est entièrement synchrone et toutes les impulsions ont une
durée plus longue que la période d'horloge. Il a les caractéristiques
suivantes :\
[4 Entrée:]{.underline}

-   3 Boutons poussoirs \"BP0\",\"BP1\",\"BP2\" servant à écrire un code

-   1 entrée de verrouillage du coffre \"V\" (V=1 reverrouille le
    coffre).

    -   Attention cette entrée ne provoque rien si le coffre n'est pas
        ouvert

[1 Sortie:]{.underline}

-   1 signal d'ouverture du coffre (S=1 : Ouvre le coffre)

[4 Etats:]{.underline}

-   E0: pas de bouton pressé

-   E1: \"BP0\" observé

-   E2: \"BP0 BP1\" observé

-   E3: \"BP0 BP1 BP2\" observé / Coffre ouvert

ATTENTION: La saisie du code doit être recommencé si 2 boutons sont
appuyés en même temps (Le système associe ceci à une erreur).

ATTENTION bis: Par erreur de lecture, les boutons ne sont pas
\"BP1\",\"BP2\",\"BP3\" comme dans le cahier des charges originel mais
\"BP0\",\"BP1\",\"BP2\".

# Graphe d'état(Conception de Moore)

Voici le graphe d'état associé au système :

::: center
![image](assets/img/projects/safe_opening_system/graph.jpg){height="10cm"}\
:::

# Obtention de l'expression des entrées des bascules et de la sortie

## Table de transition

A partir du graphe d'état précédent, on obtient la table de transition
suivante :

::: center
![image](assets/img/projects/safe_opening_system/transition.jpg){height="10cm"}\
:::

## Table de Karnaugh

### 

Table de Karnaugh de $e_{0}^+$ A partir de la table de transition
précédente, on obtient la table de Karnaugh de $e_{0}^+$ :

::: center
![image](assets/img/projects/safe_opening_system/karnaugh_e0.jpg){height="9cm"}\
:::

### Table de Karnaugh de $e_{1}^+$

A partir de la table de transition précédente, on obtient la table de
Karnaugh de $e_{1}^+$ :

::: center
![image](assets/img/projects/safe_opening_system/karnaugh_e1.jpg){height="9cm"}\
:::

### Obtention de l'expression de la sortie

Par lecture de de la table de transition précédente, on peut rapidement
déduire que l'équation de la sortie S est $S = e_{0}.e_{1}$

# Conception du systèmes avec des bascules D

A partir des équations précédentes, on réalise le circuit suivant:

::: center
![image](assets/img/projects/safe_opening_system/circuitE1.jpg){height="7cm"}\
:::

::: center
![image](assets/img/projects/safe_opening_system/circuitE2.jpg){height="7cm"}\
:::

::: center
![image](assets/img/projects/safe_opening_system/circuitS.jpg){height="5cm"}\
:::

# Simulation et test du système sur LTSpice

Afin de tester le circuit précédent on élabore un scénario de test
menant à la production de la simulation suivante :

::: center
![image](assets/img/projects/safe_opening_system/simu.jpg){height="9cm"}\
:::

Voici le scénario de test (les étapes liés au texte sont notézs sur la
simulation précédente) :

-   Etape (1) :\
    L'opérateur appuie sur \"BP0\", on passe bien dans E1
    ($e_{1}=0 et e_{1}=1$). Puis l'opérateur appuie sur \"V\" rien ne se
    passe comme prévu puisque V ne doit rien provoqué si le coffre n'est
    pas ouvert.\

-   Etape (2) :\
    On est toujours E1 ($e_{1}=0 et e_{1}=1$). L'opérateur appuie sur
    \"BP0\" et \"BP1\" au même moment, on retourne dans E0
    ($e_{1}=0 et e_{1}=0$). Le circuit a détecté une erreur, il faut
    recommencer le code.\

-   Etape (3) :

    -   L'opérateur appuie sur \"BP0\", on passe bien dans E1
        ($e_{1}=0 et e_{1}=1$).

    -   L'opérateur appuie sur \"BP1\", on passe bien dans E2
        ($e_{1}=1 et e_{1}=0$).

    -   L'opérateur appuie sur \"BP2\", on passe bien dans E3
        ($e_{1}=1 et e_{1}=1$) et le coffre est ouvert (S=1).

      \

-   Etape (4) :\
    V est mise à l'état haut, on retourne dans E0
    ($e_{1}=0 et e_{1}=0$), le coffre est fermé et S=0.
