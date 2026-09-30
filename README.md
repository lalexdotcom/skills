# skills

Skills pour agents de code, installables avec la CLI [`skills`](https://skills.sh).

## Installation

```bash
npx skills add lalexdotcom/skills --list          # lister les skills disponibles
npx skills add lalexdotcom/skills                 # choix interactif
npx skills add lalexdotcom/skills -s <nom> -g     # un skill précis, en global
npx skills add lalexdotcom/skills --all           # tout installer
npx skills update                             # mettre à jour
```

## Ajouter un skill

Chaque skill est un dossier de `skills/` contenant un `SKILL.md` :

```
skills/
└── mon-skill/
    ├── SKILL.md
    └── references/    (optionnel : fichiers annexes, scripts)
```

```markdown
---
name: mon-skill
description: Ce que fait le skill et quand le déclencher.
---

Instructions du skill…
```

- `name` : minuscules et tirets, identique au nom du dossier, unique dans le repo.
- `description` : décide du déclenchement du skill par l'agent, elle doit donc être précise.

`npx skills init <nom>` génère un gabarit. Pour vérifier la détection avant de pousser :

```bash
npx skills add . --list
```
