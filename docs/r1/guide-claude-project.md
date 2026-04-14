# Guide de configuration — Claude Project

## Prérequis

- Compte Claude Pro ou Team sur https://claude.ai
- Accès à la fonctionnalité "Projects"

## Étapes

### 1. Créer un nouveau projet

- Aller sur https://claude.ai
- Cliquer sur "Projects" dans le menu latéral
- Cliquer "Create Project"

### 2. Remplir les champs

**Nom du projet :**
```
Synthèse R1 — Renée Costes
```

**Description :**
```
Assistant pour conseillers experts Renée Costes. Génère la fiche projet, l'email client et l'analyse des freins après un premier rendez-vous (R1) viager.
```

**Custom Instructions :**

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

### 4. Activer l'intégration Gmail

- Dans la conversation, Claude peut utiliser l'intégration Gmail (MCP)
- Lors de la première utilisation, Claude demandera l'autorisation de se connecter à Gmail
- Accepter la connexion pour permettre la création de brouillons
- L'assistant pourra alors créer un brouillon directement dans Gmail quand l'utilisateur le demande

### 5. Tester

- Ouvrir une nouvelle conversation dans le projet
- Utiliser le scénario de démo (voir `docs/assistants/scenario-demo.md`)
- Vérifier que la fiche projet, l'email et l'analyse des freins sont générés correctement
- Tester la création d'un brouillon Gmail
