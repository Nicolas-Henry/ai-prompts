# Test — Debug PHP simple

## Modèle conseillé

Deepseek Debug

## Prompt

```text
[MODEL: Deepseek Debug]

Tu es un expert PHP.

Analyse uniquement, ne corrige pas tout de suite.

Erreur :
Fatal error: Uncaught Error: Call to undefined function format_price() in /var/www/html/controllers/ProductController.php:42

Code :

<?php

class ProductController {
    public function show($price) {
        return format_price($price);
    }
}

Objectif :
ÉTAPE 1 — Diagnostic complet
- cause probable
- niveau de certitude
- ce qu’il faut vérifier

Contraintes :
- ne pas corriger
- ne pas inventer de fichiers
- ne pas utiliser d’outil
```

## Résultat attendu

- Diagnostic clair.
- Pas de correction directe.
- Pas de lecture de fichier.
- Pas de terminal.
- Pas d’invention de framework.
