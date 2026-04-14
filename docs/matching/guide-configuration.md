# Guide de configuration — Workflow Sim.ai

## Prérequis

- Compte Sim.ai actif
- Google Sheet importé avec les 2 onglets (voir `data/mandats-vendeurs.csv` et `data/acquereurs.csv`)
- Compte Gmail connecté à Sim.ai (david+xxx@colette.club)

## Étape 1 — Créer le Google Sheet

1. Créer un nouveau Google Sheet nommé **"Masterclass IA — Matching Viager"**
2. Renommer le premier onglet → **"Mandats vendeurs"**
3. Importer `data/mandats-vendeurs.csv` (Fichier → Importer → sélectionner le CSV → séparateur point-virgule)
4. Créer un second onglet → **"Acquéreurs"**
5. Importer `data/acquereurs.csv` dans cet onglet
6. Vérifier que les colonnes s'affichent correctement (pas de fusion de cellules)
7. **Supprimer la ligne de données dans "Mandats vendeurs"** — garder uniquement l'en-tête (la ligne sera ajoutée en live pendant la démo)

## Étape 2 — Créer le workflow dans Sim.ai

1. Créer un nouveau workflow nommé **"Matching Vendeur ↔ Acquéreurs"**

## Étape 3 — Nœud 1 : Trigger Google Sheet

1. Ajouter un nœud **Google Sheets Trigger**
2. Connecter votre compte Google
3. Sélectionner le Google Sheet **"Masterclass IA — Matching Viager"**
4. Sélectionner l'onglet **"Mandats vendeurs"**
5. Événement : **Nouvelle ligne ajoutée**
6. Mapper les colonnes aux variables : `nom_vendeur`, `type`, `localisation`, `surface`, `bouquet`, `rente`, `occupation`, `description`

## Étape 4 — Nœud 2 : LLM Extraction

1. Ajouter un nœud **LLM** (AI/Chat)
2. Copier-coller le **Prompt 1** depuis `prompts.md`
3. Remplacer les `{{...}}` par les variables du trigger (étape 3)
4. Format de sortie : JSON

## Étape 5 — Nœud 3 : Lire les acquéreurs

1. Ajouter un nœud **Google Sheets Read**
2. Sélectionner le même Google Sheet
3. Sélectionner l'onglet **"Acquéreurs"**
4. Lire toutes les lignes

## Étape 6 — Nœud 4 : LLM Matching + Emails

1. Ajouter un nœud **LLM** (AI/Chat)
2. Copier-coller le **Prompt 2** depuis `prompts.md`
3. `{{json_bien}}` = sortie du nœud 2
4. `{{liste_acquéreurs}}` = sortie du nœud 3
5. Format de sortie : JSON

## Étape 7 — Nœud 5 : Envoyer les emails

1. Ajouter un nœud **Gmail Send**
2. Connecter votre compte Gmail
3. Itérer sur le JSON de sortie du nœud 4
4. Filtrer : uniquement les entrées avec `match: true`
5. Champs :
   - **To** : `{{email}}`
   - **Subject** : `{{objet_email}}`
   - **Body** : `{{corps_email}}`

## Étape 8 — Tester

1. Activer le workflow
2. Ajouter la ligne Mme Dubois dans l'onglet "Mandats vendeurs"
3. Vérifier que le workflow s'exécute
4. Vérifier dans Gmail que 3 emails arrivent (Sophie, Jean, Alain)
5. Vérifier que Marc et Claire n'ont PAS reçu d'email
6. **Supprimer à nouveau la ligne Mme Dubois** pour que le Sheet soit prêt pour la démo
