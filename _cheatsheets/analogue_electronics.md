---
layout: page
title: Electronique analogique
importance: 2
---

# Rappels d\'Electronique
## Dipôles de Base
### Resistance

![](assets/img/cheatsheets/analogue_electronics/resistor.svg){.align-center width="180px"}

-   Modèle : $u(t)=Ri(t)$
-   Impedance généralisée : $Z_R=R$

### Condensateur

![](assets/img/cheatsheets/analogue_electronics/capacitor.svg){.align-center width="180px"}

-   Modèle : $i(t)=C\frac{du(t)}{dt}$
-   Impedance généralisée : $Z_C=\frac{1}{Cp}$

### Bobine

![](assets/img/cheatsheets/analogue_electronics/inductor.svg){.align-center width="180px"}

-   Modèle : $u(t)=L\frac{di(t)}{dt}$
-   Impedance généralisée: $Z_L=Lp$

## Associations de dipôles
### Mise en série

![](assets/img/cheatsheets/analogue_electronics/serie.svg){.align-center width="200px"}

-   Impedance généralisée équivalente :

> [Z](){eq}=Z_1+Z_2

### Mise en parallèle
![](assets/img/cheatsheets/analogue_electronics/parallel.svg){.align-center width="200px"}

-   Impedance généralisée équivalente :

> frac{1}{[Z](){eq}}=frac{1}{Z_1}+frac{1}{Z_2}

### Pont diviseur
![](assets/img/cheatsheets/analogue_electronics/voltage_divider.svg){.align-center width="200px"}

-   Mise en équation :

> frac{V_2(p)}{V_1(p)}=frac{Z_2}{Z_1+Z_2}

### Potentiel des noeuds
![](assets/img/cheatsheets/analogue_electronics/node.svg){.align-center width="300px"}

-   Mise en équation :

> frac{V_1(p)-V_A(p)}{Z_1}+frac{V_2(p)-V_A(p)}{Z_2}+frac{V_3(p)-V_A(p)}{Z_3}=0

## Exemple

On considère le circuit suivant :

![](assets/img/cheatsheets/analogue_electronics/MFB_BP2.svg){.align-center width="300px"}

### Mise en équation

Soit V la tension aux bornes de $R_2$. Cette tension représente le
potentiel du noeud d\'entrée du circuit.

-   Equation 1 (loi des noeuds)

> frac{V_e(p) - V(p)}{R_1} + frac{0-V(p)}{R_2}+frac{V_s(p) -
> V(p)}{[Z](){C2}}+frac{V\^-(p) - V(p)}{[Z](){C1 }} =0

-   Equation 2 (loi des noeuds)

> frac{V(p) - [V]()-(p)}{[Z](){C1}} + frac{V_s(p)-[V]()-(p)}{R_3} =0

-   Equation 3 (AOP regime linéaire)

> [V]()+(p) = [V]()-(p)

-   Equation 4 (entrée +):

> [V]()+(p) = 0

### Fonction de transfert

Pour obtenir la fonction de transfert, nous allons déterminer une
équation avec que des termes en $V_e(p)$ d\'un côté et que des termes en
$V_s(p)$ de l\'autre côté.

En manipulant les 4 équations, nous obtenons :

> frac{V_e(p)}{R_1} = -frac{V_s(p)}{[Z](){C2}} +frac{V(p)}{[Z](){C2}}+
> frac{V(p)}{R_2}+ frac{V(p)}{[Z](){C1 }} + frac{V(p)}{R_1}

> V(p) = -frac{[Z](){C1}}{R_3}V_s(p)

Il en vient que

> frac{V_e(p)}{R_1} = -V_s(p)left(frac{1}{[Z](){C2}}
> -frac{[Z](){C1}}{[Z](){C2}R_3} -frac{[Z](){C1}}{R_2R_3}-frac{1}{R_3}
> -frac{[Z](){C1}}{R_1R_3}right)

En remplaçant les impédances par leur expressions et en mettant tout
sous le même denominateur pour le terme de droite, nous obtenons

> frac{V_e(p)}{R_1} = -frac{V_s(p)}{R_1R_2R_3C_1p} left(
> R_1R_2R_3C_1C_2p\^2 + R_1R_2C_2p + R_1 + R_1R_2C_1p + R_2right)

Finalement,

> H(p) = frac{V_s(p)}{V_e(p)} = -frac{frac{R_2R_3}{R_1 + R_2}C_1p}{
> frac{R_1R_2R_3}{R_1 + R_2}C_1C_2p\^2 + frac{R_1R_2}{R_1 +
> R_2}(C_1+C_2)p + 1}
