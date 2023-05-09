# Documentation

Le format « doxygen » permet de générateur automatiquement de la documentation à partir de commentaires dans le code source :

## Fichiers

Tous les fichiers doivent avoir un en-tête :

```cpp
/// @file Fichier.ext
/// @brief Brève description.
/// @authors Prénom Nom, Prénom Nom, ...
```

## Classes

Toutes les déclarations de classe doivent avoir un en-tête :

```cpp
/// @class Classe
/// @brief Brève description.
/// @tparam Modele Description du paramètre modèle
template <typename Modele>
class Classe {
  // ...
};
```

## Variables et Données membres

Toutes les variables et données membres doivent être suivies d'une brève description :

```cpp
int variable; ///< Description.
```

## Fonctions et Méthodes

Toutes les fonctions et méthodes doivent avoir un en-tête :

```cpp
/// @brief Brève description.
/// @param parametreA Description du paramètre A.
/// @param parametreB Description du paramètre B.
/// @return Description du retour.
int fonction(int parametreA, float parametreB) {
  // ...
  return resultat;
}
```
