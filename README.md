# AI Prompts

Bibliothèque publique de prompts, règles et snippets pour travailler plus efficacement avec des assistants IA de développement comme Continue, Ollama, Codex ou Claude Code.

Ce dépôt me sert à centraliser, sauvegarder et versionner mes prompts utilisés pour le debug, la correction de code, le refactor PHP, les tests de modèles et les workflows multi-modèles.

## Objectifs

- Centraliser les prompts utiles au quotidien.
- Gagner du temps avec des prompts prêts à copier-coller.
- Tester plusieurs modèles sur des cas identiques.
- Garder un historique des prompts qui fonctionnent bien.
- Sauvegarder les snippets VS Code utilisés avec Continue.
- Documenter un workflow IA plus fiable pour le développement PHP.

## Structure du dépôt

```text
ai-prompts/
├── README.md
├── continue/
│   ├── 00-agent-securise.md
│   └── 10-contexte-fourni.md
├── models/
│   ├── deepseek-debug.md
│   ├── qwen-30b-local.md
│   ├── qwen-480b-cloud.md
│   └── qwen-next-cloud.md
├── php/
│   ├── correction.md
│   ├── debug.md
│   ├── multi-files.md
│   └── refactor.md
├── snippets/
│   ├── prompt-master-session.txt
│   ├── quick-debug.txt
│   └── strict-mode.txt
├── tests/
│   ├── test-debug.md
│   ├── test-modeles.md
│   └── test-multifichiers.md
└── vscode/
    └── ai-prompts.code-snippets
```

## Snippets VS Code

Le fichier de snippets est disponible ici :

[Voir le fichier `ai-prompts.code-snippets`](https://github.com/Nicolas-Henry/ai-prompts/blob/main/vscode/ai-prompts.code-snippets)

Ces snippets permettent d’insérer rapidement des prompts dans VS Code, par exemple :

```text
dbgphp     → prompt de debug PHP avec Deepseek
fixphp     → prompt de correction PHP avec Qwen 30B
expphp     → prompt d’explication simple
safeagent  → mode agent sécurisé
```

## Installer les snippets dans VS Code

Dans VS Code :

1. Ouvrir la palette de commandes :

```text
Ctrl + Shift + P
```

2. Chercher :

```text
Preferences: Configure User Snippets
```

3. Créer un fichier global :

```text
ai-prompts.code-snippets
```

4. Copier le contenu du fichier :

```text
vscode/ai-prompts.code-snippets
```

## Workflow recommandé avec Continue + Ollama

Ce dépôt est pensé pour un usage avec plusieurs modèles, chacun ayant un rôle précis.

```text
Deepseek Debug Cloud   → diagnostic / analyse d’erreur
Qwen 30B Local         → correction / édition / apply
Qwen Next Cloud        → explication rapide / reformulation
Qwen 480B Cloud        → cas complexe ponctuel
Codex / Claude Code    → gros refactor ou chantier multi-fichiers
```

## Exemple de workflow debug PHP

### 1. Diagnostic avec Deepseek

Utiliser le snippet :

```text
dbgphp
```

Objectif :

- comprendre l’erreur ;
- identifier la cause probable ;
- éviter les corrections trop rapides ;
- ne pas utiliser d’outil inutilement.

### 2. Correction avec Qwen 30B

Utiliser le snippet :

```text
fixphp
```

Objectif :

- corriger uniquement ce qui est nécessaire ;
- éviter le refactor inutile ;
- ne pas inventer de fichier ;
- fournir une correction minimale.

## Règles Continue

Le dossier `continue/` contient des règles pour encadrer le comportement de l’agent :

```text
continue/00-agent-securise.md
continue/10-contexte-fourni.md
```

Ces règles servent à limiter les comportements indésirables :

- lecture de fichiers non demandée ;
- usage inutile du terminal ;
- hallucination de fichiers ;
- refactor trop large ;
- correction sans diagnostic préalable.

## Tests de modèles

Le dossier `tests/` contient des prompts de test pour comparer plusieurs modèles sur un même problème.

Exemple :

```text
tests/test-modeles.md
```

Ce fichier permet de comparer :

- Deepseek Debug ;
- Qwen 30B Local ;
- Qwen Next Cloud ;
- Qwen 480B Cloud.

## Sécurité

Ce dépôt est public.

Ne jamais y stocker :

- clés API ;
- tokens GitHub ;
- mots de passe ;
- informations client ;
- code propriétaire sensible ;
- configuration privée contenant des secrets ;
- exports complets de conversations privées.

Les prompts doivent rester génériques ou anonymisés.

## Usage personnel

Ce dépôt est principalement une bibliothèque personnelle de prompts et de workflows IA.

Il peut cependant servir d’exemple à d’autres développeurs souhaitant organiser leurs prompts, snippets et tests de modèles pour un usage avec VS Code, Continue, Ollama, Codex ou Claude Code.
