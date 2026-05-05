# Test — Comparaison de modèles

## Test 1 — Deepseek Debug

```text
[MODEL: Deepseek Debug]

Analyse uniquement cette erreur PHP :

Fatal error: Uncaught Error: Call to undefined function format_price()

Code :

<?php

class ProductController {
    public function show($price) {
        return format_price($price);
    }
}

Ne corrige pas. Donne uniquement le diagnostic.
```

## Test 2 — Qwen 30B Local

```text
[MODEL: Qwen 30B Local]

À partir du diagnostic précédent, propose une correction minimale.

Contraintes :
- pas de nouveau fichier ;
- pas de framework supposé ;
- pas de refactor ;
- code corrigé uniquement puis explication courte.
```

## Test 3 — Qwen Next Cloud

```text
[MODEL: Qwen Next Cloud]

Explique cette erreur PHP à un débutant en 5 lignes maximum.
```

## Test 4 — Qwen 480B Cloud

```text
[MODEL: Qwen 480B Cloud]

Propose une correction propre et légèrement améliorée, sans architecture complexe.
```

## Points à observer

- Respect des consignes.
- Absence d’hallucination.
- Pas de lecture de fichier si code fourni.
- Pertinence de la correction.
- Capacité à rester minimaliste.
