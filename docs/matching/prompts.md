# Prompts LLM — Workflow Sim.ai Matching

> Copier-coller ces prompts dans les nœuds LLM du workflow Sim.ai.

---

## Prompt 1 — Extraction des caractéristiques du bien

> À utiliser dans le premier nœud LLM, après le trigger Google Sheet.
> Les variables `{{...}}` correspondent aux colonnes du Google Sheet "Mandats vendeurs".

```
Analyse cette fiche de mandat vendeur et extrais un JSON structuré :

Nom vendeur : {{nom_vendeur}}
Type : {{type}}
Localisation : {{localisation}}
Surface : {{surface}}
Bouquet estimé : {{bouquet}}
Rente estimée : {{rente}}
Occupation : {{occupation}}
Description : {{description}}

Retourne uniquement un JSON valide avec ces champs :
{
  "type_bien": "...",
  "ville": "...",
  "arrondissement": "...",
  "surface_m2": 85,
  "bouquet_euros": 90000,
  "rente_euros": 800,
  "occupation": "occupé",
  "points_forts": ["...", "..."],
  "points_attention": ["..."]
}
```

---

## Prompt 2 — Matching acquéreurs + rédaction emails

> À utiliser dans le second nœud LLM, après la récupération de la liste acquéreurs.
> `{{json_bien}}` = sortie du Prompt 1.
> `{{liste_acquéreurs}}` = données lues depuis le Google Sheet "Acquéreurs".

```
Tu es un assistant Renée Costes spécialisé en viager.

Voici un nouveau bien en mandat :
{{json_bien}}

Voici la liste des acquéreurs :
{{liste_acquéreurs}}

Pour chaque acquéreur, analyse la compatibilité en tenant compte de :
- Zone géographique (correspondance ville/région)
- Budget bouquet (le bouquet estimé du bien doit être ≤ budget max de l'acquéreur)
- Type de bien souhaité
- Occupation souhaitée (occupé/libre)
- Critères libres (analyse sémantique)

Pour chaque acquéreur qui matche, rédige un email personnalisé :
- Objet : "Nouveau bien en viager — {{localisation}}"
- Ton : professionnel, chaleureux, personnalisé
- Mentionne le prénom de l'acquéreur
- Explique pourquoi ce bien correspond à SES critères spécifiques
- Décris brièvement le bien (sans donner le nom du vendeur)
- Invite à prendre contact pour en savoir plus
- Signature : Marc Dupont, Conseiller Expert — Renée Costes

Retourne uniquement un JSON valide :
[
  {
    "prenom": "...",
    "email": "...",
    "match": true,
    "raison": "...",
    "objet_email": "...",
    "corps_email": "..."
  },
  {
    "prenom": "...",
    "email": "...",
    "match": false,
    "raison": "..."
  }
]

Important : inclus TOUS les acquéreurs dans le JSON (match true ET false). Pour les non-matchs, ne génère pas d'email.
```
