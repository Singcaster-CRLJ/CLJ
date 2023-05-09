# Normes de programmation JavaScript

Les règles suivantes s'ajoutent aux [normes départementales](Normes.md).

## Variables

Les variables doivent être déclarés avec le mot-clé `let`. Le mot-clé `var` ne doit pas être utilisé.

```js
// var nombres = 0;
let nombres = 0;
```

## Mode strict

En haut (1ère ligne) de chaque fichier JavaScript inclus dans le HTML, il faut activer le mode strict:

```js
"use strict";

// Code Javascript par la suite
```

## Point-virgule

Bien que le point-virgule est optionnel en majorité, il faut l'inclure à la fin de toutes les lignes ne finissants par par une accolade.

```js
// let nb = 42
let nb = 42;

function toto() {
    // return "toto"
    return "toto";
}
```