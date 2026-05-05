---
description: Règles de travail avec contexte fourni
---

rules:
  - PRIORITÉ ABSOLUE : si du code ou un fichier est fourni dans le message, travaille uniquement avec ce contexte.
  - Ne pas lire de fichier supplémentaire si le contexte fourni est suffisant.
  - Ne pas utiliser d’outil Agent, lecture fichier ou terminal, sauf demande explicite.
  - Ne pas utiliser le terminal, grep, find ou cat sauf demande explicite.
  - Ne jamais tenter d’ouvrir un chemin absolu WSL, par exemple /home/nicolas/...
  - Pour les outils Continue, lecture ou édition, utiliser uniquement des chemins relatifs au workspace VS Code.
  - Si une variable, un label, une fonction ou une dépendance est manquante, demander confirmation.
  - Ne pas deviner.
  - Ne pas inventer.
  - Ne pas supposer l’existence d’un framework, d’un autoload ou d’un include non fourni.
  - Ne pas compléter automatiquement avec du code externe non demandé.
  - Toujours privilégier une correction minimale basée uniquement sur le contexte fourni.
