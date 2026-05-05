# Modèle conseillé — Qwen 480B Cloud

Usage conseillé :

- cas complexe ponctuel ;
- analyse plus profonde ;
- refactor conceptuel ;
- exploration de solutions.

Attention :
Ce modèle peut être lent ou dépendre de la charge du cloud Ollama. À utiliser ponctuellement, pas forcément comme modèle principal.

Prompt de test :

```text
[MODEL: Qwen 480B Cloud]

Voici une version plus réaliste :

<?php

class ProductController {

    public function show($price) {
        return format_price($price);
    }

}

Objectif :
- proposer une correction propre
- proposer une version légèrement améliorée
- expliquer brièvement les choix

Contraintes :
- rester simple
- ne pas créer d’architecture complexe
```
