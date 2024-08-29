# Normes pour système de gestion de versions

Les normes départementales de ce document doivent être respectées dans tous les cours utilisant un système de gestion de versions.

## Techniques

...

## Structure

À la racine de votre dépôt de données (repository), il doit y avoir un fichier README.md contenant votre nom complet.

Les fichiers innutiles aux remises doivent être absents du dépôt de données ou dans le fichier .gitignore.
Comme exemple : les dossiers de configuration vscode et jetbrains, les journaux, les fichiers générés par un gestionnaire de dépendances composer et nugget, etc.

Évitez les sous-dossiers inutiles. Un dépôt de donnée d'un seul projet devrait avoir son fichier principal d'exécution à la racine.

Ne pas quantifier ou qualifier vos dossiers : TP1_v5, TP1_Bon, etc.

Ne pas téléverser de fichiers compressés : .zip, .7z, etc.

## Message de soumission

Les messages de soumissions doivent être significatifs, clairs et concis.

```
Type (Portée) - Sujet
```

*Un message détaillé est optionnel si nécessaire.*

### Type

|Type |Description|
|-----|-----------|
|Ajout|Ajout d'une nouvelle fonctionnalité, de fichiers, etc.|
|Conflit|Gestion de conflit, etc.|
|Correction|Correction d'un problème, d'un bogue, etc.|
|Divers|Configuration de projet, de compilation, etc.|
|Documentation|Documentation, commentaires, etc.|
|Réorganisation|Réorganisation, changement de paradigme, etc.|
|Test|Test, exemple, etc.|
|...|...|

### Portée

Ce qui est affecté par la soumission.

### Sujet

Brève (pas plus de 80 caractères) description de la soumission.
