# Guide de configuration — Gemini Gem

## Prérequis

- Compte Google One AI Premium (Gemini Advanced)
- Accès au Gem Manager sur https://gemini.google.com

## Étapes

### 1. Créer un nouveau Gem

- Aller sur https://gemini.google.com
- Cliquer sur "Gem manager" dans le menu latéral
- Cliquer "New Gem"

### 2. Remplir les champs

**Name :**
```
Synthèse R1 — Renée Costes
```

**Instructions :**

Copier-coller l'intégralité du prompt depuis `docs/assistants/prompt-maitre.md` (tout le contenu après le séparateur `---`).

**Conversation starters :**

```
J'ai mes notes du R1, génère la synthèse complète
```
```
Analyse les freins de mon client
```
```
Rédige la fiche projet à partir de mes notes
```
```
Rédige l'email de suivi pour mon client
```

### 3. Knowledge files

Charger le fichier `reference-viager.md` (fondamentaux viager + argumentaire objections).

### 4. Activer l'extension Gmail

- Dans les paramètres Gemini → Extensions
- Activer l'extension **Google Workspace**
- Cela permet au Gem de créer des brouillons dans Gmail
- Lors de la démo, demander explicitement au Gem de créer le brouillon dans Gmail

### 5. Sauvegarder et tester

- Cliquer "Save"
- Ouvrir une conversation avec le Gem
- Utiliser le scénario de démo (voir `docs/assistants/scenario-demo.md`)
- Vérifier que la fiche projet, l'email et l'analyse des freins sont générés correctement
- Tester la création d'un brouillon Gmail
