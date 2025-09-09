# Normes de programmation

Les normes départementales de ce document doivent être respectées dans tous les cours et langages de programmation où elles peuvent s'appliquer.

Règles spécifiques:

  - [JavaScript](NormesJS.md)

## Langue

Le code peut être en anglais ou en français, mais doit être constant. Tandis que la documentation, les commentaires, et les interfaces utilisateurs doivent obligatoirement être en français.

## Inclusions ##

Limiter les inclusions, importations, utilisations, etc. à ce qui est nécessaire au code présent dans le fichier :

```cpp
#include <iostream>
// ^^^^^^^^^^^^^^^^ Ne devrait pas être présent puisqu'inutilisé.

int main() {
  return 0;
}
```

## Identificateurs

Les identificateurs de structure, classe, constante, donnée membre, variable, méthode, et fonction doivent être significatifs.

De plus, pour une meilleure intercompatibilité, les règles suivantes devraient être respectées :

- Débuter par une lettre ou un trait de soulignement « _ ».
- Contenir que des lettres, des chiffres, et des traits de soulignement « _ ». (Pas d'accents, ni de caractères spéciaux.)
- Ne pas être un terme réservé par les langages de programmation.

### Constantes

Pour être plus distinguables des autres identificateurs, ceux des constantes doivent contenir que des lettres majuscules, et des traits de soulignement « _ » pour séparer les termes :

```cpp
#define TAILLE_MAXIMALE 42
```

### Variables

Les identificateurs de données membres, de variables, de méthodes, et de fonctions, doivent utiliser la casse de chameau « camel case », c'est-à-dire commencer par un caractère minuscule, et utiliser un caractère majuscule au début des termes suivants :

```cpp
bool identificateurDeVariableBooleenne = true;
```

### Fonctions

Une fonction ne devrait pas contenir moins de deux lignes, et au maximum une trentaine de lignes de code. Il est conseillé que son identificateur comporte un verbe à l'infinitif précisant ce que réalise la fonction.

Les paramètres devraient être ordonnés de sorte à pouvoir définir le plus d'arguments par défaut possible afin de réduire le nombre de paramètres de chacune des fonctions.

### Classes

Les identificateurs d'espace de nom, de structure, de classe, etc., doivent utiliser la casse pascal « studle caps », en débutant par un caractère majuscule :

```cpp
class Utilisateur {};
class SuperUtilisateur {};
```

## Propreté

Tout code source doit être le plus concis possible, tout en restant visuellement agréable et facile à lire.

Les remises ne devraient pas contenir de code de débogage.

### Aération

Comme dans tous textes, les gros morceaux de code doivent être séparés en paragraphes afin d'être plus agréables à lire, mais il ne devrait pas y avoir plus de 2 sauts de lignes consécutifs.

Chaques éléments importants doivent aussi être séparés par une ligne vide. Par exemple: entre les inclusions et la classe, entre les constantes et les propriétés, entre les propriétés et méthodes et entre chaque méthodes.

Les opérateurs unaires doivent être adjacents aux identificateurs tandis que les opérateurs binaires doivent être précédés et suivis d'un espace :

```cpp
int variableC = ++variableA * variableB++;
```

### Commentaires

Seul les morceaux de code non triviaux ou redondants doivent être commentés afin d'expliquer leur algorithme.

Les remises ne devraient pas contenir de code en commentaire inutilement.

### Indentation

Il doit y avoir une indentation suite aux accolades ouvrantes, aux modificateurs d'accès, aux if, aux else, aux while, aux for, et aux case :

```cpp
class Classe {
public:
  void methode(int valeurEntiere) {
    switch (valeurEntiere) {
    default:
      for (int i = 0; i < 1000; i++)
        if (valeurEntiere < 42)
          valeurEntiere++;
        else
          valeurEntiere--;          
      break;
    }
  }
};
```

L'indentation doit être faite avec des tabulations.

### Accolades

L'accolade ouvrante ( `{` ) doit être à la fin de la ligne et précédé d'un espace :

```cpp
if (proposition) {
  // Instructions
}
```

### Pléonasmes

Évitez les pléonasmes de programmeur :

```cpp
// if (estValide == true) {}
if (estValide) {}

// if (count != 0) {}
if (count) {}

/*
if (estValide)
  enMarche = true;
else
  enMarche = false;
*/
enMarche = estValide;
```

### Redondance

Évitez les redondances et les lignes inutiles :

```cpp
/*
if (estValide) {
  instructionA();
  instructionC();
}
else {
  instructionB();
  instructionC();
}
*/
if (estValide)
  instructionA();
else
  instructionB();
instructionC();

int fonction() {
  if (estValide)
    return 42;
  // else
  return -1;
}
```


