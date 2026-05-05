# Modèle conseillé — Deepseek Debug

Usage conseillé :

- diagnostic d’erreur ;
- analyse PHP ;
- explication de stacktrace ;
- hypothèses de correction.

Prompt de test :

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
