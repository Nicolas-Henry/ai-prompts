# Test — Simulation multi-fichiers PHP

## Objectif

Tester un modèle sur une correction qui semble multi-fichiers, tout en vérifiant qu’il ne modifie pas tout sans justification.

## Prompt

```text
[MODEL: Qwen 30B Local]

Tu es en mode agent sécurisé.

Contexte :

Fichier : public/index.php

<?php

require_once __DIR__ . '/../controllers/ProductController.php';

$controller = new ProductController();
echo $controller->show(12.5);

Fichier : controllers/ProductController.php

<?php

class ProductController {
    public function show($price) {
        return format_price($price);
    }
}

Erreur :
Fatal error: Uncaught Error: Call to undefined function format_price()

Objectif :
- analyser la cause ;
- proposer une correction minimale ;
- ne pas créer d’architecture complexe.

Contraintes :
- travailler uniquement avec les deux fichiers fournis ;
- ne pas lire d’autres fichiers ;
- ne pas utiliser d’outil ;
- ne pas inventer de framework ;
- proposer le code corrigé.
```

## Résultat attendu

- Le modèle identifie que `format_price()` n’existe pas.
- Il propose soit d’ajouter une fonction minimale, soit d’utiliser `number_format()`.
- Il ne crée pas de service, helper, composer autoload ou framework imaginaire.
