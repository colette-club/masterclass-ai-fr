# Guide de configuration — ChatGPT GPT

## Prérequis

- Compte ChatGPT Plus ou Team
- Accès au GPT Builder (menu latéral → "Explore GPTs" → "Create")

## Étapes

### 1. Créer un nouveau GPT

- Aller sur https://chatgpt.com/gpts/editor
- Cliquer sur "Create" dans le menu latéral
- Passer en onglet **"Configure"** (pas "Create" qui est le mode conversationnel)

### 2. Remplir les champs

**Name :**
```
Synthèse R1 — Renée Costes
```

**Description :**
```
Assistant pour conseillers experts Renée Costes. Génère la fiche projet, l'email client et l'analyse des freins après un premier rendez-vous (R1) viager.
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

### 3. Configurer les capabilities

- **Web Browsing** : OFF
- **DALL-E Image Generation** : OFF
- **Code Interpreter & Data Analysis** : OFF

### 4. Knowledge files

Charger le fichier `reference-viager.md` (fondamentaux viager + argumentaire objections).

### 5. Actions (Gmail)

L'intégration Gmail via Actions nécessite une configuration OAuth complexe. Pour la démo, **ne pas configurer** — l'email sera généré en texte et copié manuellement.

Si vous souhaitez tout de même tester :
- Créer une Action avec le schéma OpenAPI Gmail
- Configurer l'authentification OAuth 2.0 avec les scopes `gmail.compose`
- Cela dépasse le cadre de cette démo

### 6. Sauvegarder

- Cliquer "Save" → choisir "Only me" (usage démo personnel)
- Tester avec le scénario de démo (voir `docs/assistants/scenario-demo.md`)
