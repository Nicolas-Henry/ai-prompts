# AI Prompts

Repo privé conseillé pour centraliser, sauvegarder et versionner les prompts utilisés avec Continue, Ollama, Codex et autres assistants IA.

## Objectifs

- Copier/coller rapidement les bons prompts.
- Sauvegarder les règles et modes de travail.
- Comparer les modèles sur des tests identiques.
- Garder un historique des prompts efficaces.

## Structure

```text
ai-prompts/
├── README.md
├── php/
│   ├── debug.md
│   ├── correction.md
│   ├── refactor.md
│   └── multi-files.md
├── continue/
│   ├── 00-agent-securise.md
│   └── 10-contexte-fourni.md
├── tests/
│   ├── test-debug.md
│   ├── test-modeles.md
│   └── test-multifichiers.md
├── snippets/
│   ├── strict-mode.txt
│   ├── quick-debug.txt
│   └── prompt-master-session.txt
└── models/
    ├── deepseek-debug.md
    ├── qwen-30b-local.md
    ├── qwen-next-cloud.md
    └── qwen-480b-cloud.md
```

## Utilisation rapide

1. Ouvrir ce repo dans VS Code.
2. Copier le prompt adapté.
3. Sélectionner manuellement le bon modèle dans Continue.
4. Coller le prompt dans le chat ou l'agent.

## Choix conseillé des modèles

```text
Debug / analyse PHP      -> Deepseek Debug
Correction / modification -> Qwen 30B Local
Explication rapide        -> Qwen Next Cloud
Cas complexe ponctuel     -> Qwen 480B Cloud
Gros refactor fiable      -> Codex / Claude Code
```

## GitHub privé

```bash
git init
git remote add origin git@github.com:TON_USER/ai-prompts.git
git add .
git commit -m "init prompts"
git push -u origin main
```
