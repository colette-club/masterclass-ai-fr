# Scénario de démo — Synthèse R1

> Ce scénario contient des données **fictives** réalistes pour tester l'assistant en live.
> Copier-coller les blocs ci-dessous dans la conversation avec l'assistant.

---

## Test 1 — Synthèse complète (Mode combiné)

Copier-coller ce bloc de notes brutes :

```
rdv avec mme dubois ce matin, appart T4 rue des Lilas à Lyon 6e, 
85m2 environ, bon état général mais cuisine à refaire. 
Elle a 78 ans, veuve, vit seule dans l'appart depuis 42 ans. 
Ses 2 enfants sont à Paris, la voient peu.

Elle veut rester chez elle le plus longtemps possible mais galère 
avec sa retraite de 1 400€. Charges de copro qui augmentent.
Voisine lui a parlé du viager.

Estimation : elle pense que ça vaut 350-400k€. 
Elle voudrait un bouquet de 80-100k€ pour refaire la cuisine 
et avoir un matelas de sécurité + une rente mensuelle correcte.

Freins : son fils aîné est contre ("tu brades l'héritage"), 
elle a peur de ne plus être chez elle, 
et elle a lu des trucs négatifs sur internet.
Il y a aussi un petit souci : elle est en indivision avec 
sa belle-sœur sur une cave au sous-sol (héritage du mari).

Prochaines étapes : je lui envoie un mail récap, 
je fais l'estimation, et on se revoit dans 15 jours.
Conseiller : Marc Dupont
Date : 11 avril 2026
```

**Résultat attendu :** L'assistant génère la fiche projet, l'email client et l'analyse des freins (pression familiale, peur de dépossession, méfiance internet, indivision cave).

---

## Test 2 — Analyse des freins seule (Mode 2)

Copier-coller ce bloc :

```
Mon client M. Bernard hésite beaucoup. 
Il a 82 ans, propriétaire d'une maison à Aix.

Ses freins :
- Sa fille dit que le viager c'est "parier sur la mort de son père"
- Il a peur que l'acheteur ne paie plus la rente après quelques années
- La maison a une extension véranda construite sans permis en 1998
- Il trouve que le bouquet proposé (60k€ pour une maison à 280k€) est trop faible
- Il ne comprend pas comment on calcule la rente
```

**Résultat attendu :** 5 freins analysés (3 émotionnels : pression fille, peur non-paiement, incompréhension calcul ; 2 techniques : véranda sans permis, bouquet perçu trop faible). Plan d'action ordonné.

---

## Test 3 — Email seul (Mode email)

Copier-coller ce bloc :

```
Rédige l'email de suivi pour Mme Dubois suite au R1 du 11 avril.
On a discuté de la vente en viager de son T4 Lyon 6e.
Je vais faire l'estimation sous 10 jours et on se revoit le 25 avril.
Elle doit me fournir sa taxe foncière et ses 3 derniers relevés de charges.
Conseiller : Marc Dupont, tel 06 12 34 56 78
```

**Résultat attendu :** Email professionnel, chaleureux, en vouvoiement. Pas de jargon. Mention des prochaines étapes des deux côtés.

---

## Test 4 — Brouillon Gmail

Après avoir généré un email (test 1 ou 3), demander :

```
Mets cet email en brouillon dans Gmail
```

**Résultat attendu :** L'assistant crée un brouillon dans Gmail avec le contenu de l'email généré. (Fonctionne sur Claude Project et Gemini Gem. Non disponible sur ChatGPT GPT sans configuration Actions.)

---

## Conseils pour la démo live

1. **Commencer par le Test 1** — c'est le plus impressionnant (input brut → 3 outputs structurés)
2. **Montrer sur 2 plateformes** minimum pour illustrer la portabilité du prompt
3. **Finir par le Test 4** (Gmail) pour montrer l'intégration avec les outils existants
4. **Laisser l'audience suggérer des freins** supplémentaires pour montrer l'interactivité
