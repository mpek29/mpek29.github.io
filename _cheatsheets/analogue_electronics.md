---
layout: page
title: Electronique analogique
importance: 2
---

# Rappels d\'Electronique
## Dipôles de Base
### Resistance

{% include figure.html path="assets/img/cheatsheets/analogue_electronics/resistor.svg" class="img-fluid rounded z-depth-1" %}

-   Modèle : $$ u(t)=Ri(t) $$
-   Impedance généralisée : $$ Z_R=R $$

### Condensateur

{% include figure.html path="assets/img/cheatsheets/analogue_electronics/capacitor.svg" class="img-fluid rounded z-depth-1" %}

-   Modèle : $$ i(t)=C\frac{du(t)}{dt} $$
-   Impedance généralisée : $$ Z_C=\frac{1}{jC\omega} $$

### Bobine

{% include figure.html path="assets/img/cheatsheets/analogue_electronics/inductor.svg" class="img-fluid rounded z-depth-1" %}
-   Modèle : $$ u(t)=L\frac{di(t)}{dt} $$
-   Impedance généralisée: $$ Z_L=jL\omega $$

## Associations de dipôles
### Mise en série
{% include figure.html path="assets/img/cheatsheets/analogue_electronics/serie.svg" class="img-fluid rounded z-depth-1" %}

-   Impedance généralisée équivalente :

$$
Z_eq=Z_1+Z_2
$$

### Mise en parallèle
{% include figure.html path="assets/img/cheatsheets/analogue_electronics/parallel.svg" class="img-fluid rounded z-depth-1" %}

-   Impedance généralisée équivalente :

$$
\frac{1}{Z_eq}= \frac{1}{Z_1} + \frac{1}{Z_2}
$$

### Pont diviseur
{% include figure.html path="assets/img/cheatsheets/analogue_electronics/voltage_divider.svg" class="img-fluid rounded z-depth-1" %}

-   Mise en équation :

$$
\frac{V_2(j\omega)}{V_1(j\omega)} = \frac{Z_2}{Z_1+Z_2}
$$

### Potentiel des noeuds
{% include figure.html path="assets/img/cheatsheets/analogue_electronics/node.svg" class="img-fluid rounded z-depth-1" %}

-   Mise en équation :

$$
\frac{V_1(j\omega)-V_A(j\omega)}{Z_1} + \frac{V_2(j\omega)-V_A(j\omega)}{Z_2} + \frac{V_3(j\omega)-V_A(j\omega)}{Z_3} = 0
$$
