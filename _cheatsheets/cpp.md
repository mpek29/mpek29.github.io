---
layout: page
title: C++
importance: 4
---

## Points essentielle
Si vous avez commencez l'apprentissage de la programmation par le langage python, cas très courant de nos jours (un pense-bête y est dédié), voici quelques différences essentielles à retenir dans un premier temps :

- Il est nécessaire en C++ de place un ";" à la fin de chaque ligne (sauf si elle se termine par "{" ou "}").


## Les principaux types de données
Voici les principaux types de données.

|   **Types de données**     |         **Exemple**         |
|--------------------------  |---------------------------  |
| `int`                      | 123 ou -123                 |
| `double`                   | 19.99 ou -19.99             |
| `char`                     | 'a' ou 'B'                  |
| `string`                   | "Hello World"               |
| `bool`                     | True ou False               |

<br>

## Opérateurs
Il est possible de faire interagir les variables entre elles à l'aide d'opérateurs afin de générer des valeurs de type `bool` (qui pourront être par la suite utilisées pour faire usage d'instruction conditionnelle ou d'instruction de boucle de la forme `while` ou `for`).

| **Différents opérateurs**   | **Types de données**                                              |
|---------------------------  |------------------------------------------------------------------ |
| Opérateurs arithmétique     | `+`, `-`, `*`, `/`, `%`, `++`, `--`                               |
| Opérateurs d'assignement    | `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `^=`, `>>=`, `<<=` |
| Opérateurs de comparaison   | `==`, `!=`, `>`, `<`, `>=`, `<=`                                  |
| Opérateurs logique          | `&& `, `|| `, `!`                                                 |

<br>

## `if` Instruction conditionnelle
Une instruction conditionnelle est une instruction (appel de fonction, affectation de variable, etc.) qui sera ignorée ou considérée en fonction de la valeur du booléen placé à la suite du mot "if". Si ce booléen vaut True, l'instruction sera considérée et si ce booléen vaut False, l'instruction sera ignorée.

``` cpp
if (true) {
  cout << "Ceci sera affiché";
}else{
  cout << "Ceci ne sera pas affiché";
}
```

``` cpp
if (false) {
  cout << "Ceci ne sera pas affiché";
}else{
  cout << "Ceci sera affiché";
}
```


## Instructions de boucle
### `while`
Une instruction de boucle de la forme `while` est très proche d'une instruction conditionnelle mise à part qu'au lieu de simplement ignorer ou considérer une instruction, on va répéter en boucle l'instruction temps que la valeur du booléen n'est pas False.

``` cpp
while (true) {
  cout <<"Ceci sera répété en boucle";
}
```

``` cpp
while (false) {
  cout <<"Ceci ne sera pas répété en boucle";
}
```


### `for`
Lorsque vous savez exactement combien de fois vous voulez exécuter bloc de code, utilisez la boucle for au lieu de la boucle while :

``` cpp
for (int i = 0; i < 5; i++) {
  cout << i << "\n";
}
```

On peut également imbriquer deux boucles for (très utile lorsque l'on a une liste de liste).
``` cpp
// Outer loop
for (int i = 1; i <= 2; ++i) {
  cout << "Outer: " << i << "\n"; // Executes 2 times

  // Inner loop
  for (int j = 1; j <= 3; ++j) {
    cout << " Inner: " << j << "\n"; // Executes 6 times (2 * 3)
  }
}
```

## Fonctions

### Définition
Pour définir une fonction, on utilise le mot-clé `void` si celle-ci ne retourne aucune valeur.
Sinon, il faudra précisé le type de la donnée.
``` python
void myFunction() {
  cout << "Hello from a function";
}
```

### Appel
Pour appeler une fonction, utilisez le nom de la fonction suivi de parenthèses.
```cpp
myFunction();
```

### Arguments
Il est possible de transmettre des valeurs qui changeront à chaque appel d'une fonction à l'aide d'arguments. Ces valeurs peuvent être contenues dans des variables dont on indiquera le nom ou alors on pourra directement donner les valeurs souhaitées. Les arguments sont spécifiés après le nom de la fonction, entre parenthèses. Il n'y a pas de limites dans le nombre d'arguments, il suffit juste de les séparer entre eux à l'aide d'une virgule.

``` python
def my_function(nickname):
  print(f"Son surnom est: {nickname}")

florian_nickname = "Palpek"
my_function(florian_nickname)
my_function("La Torche")
my_function("Alphonse") 
```

``` cpp
void my_function(const std::string &nickname) {
    std::cout << "Son surnom est: " << "\n";
}

int main() {
    std::string florian_nickname = "Palpek";
    my_function(florian_nickname);
    my_function("La Torche");
    my_function("Alphonse");

    return 0;
}
```
L'exemple ci-dessus présente une fonction avec un seul argument nommé "nickname". À chaque fois que nous réalisons un appel de la fonction, nous transmettons un prénom, qui est utilisé à l'intérieur de la fonction pour afficher dans le terminal le nom complet.

## Source
- <https://www.w3schools.com/python/python_reference.asp>
