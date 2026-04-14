# Fiche déroulé — Démo Sim.ai

> Aide-mémoire pour la démo live. Imprimer ou garder sur un second écran.

---

## Checklist pré-démo

- [ ] Google Sheet ouvert — onglet "Mandats vendeurs" **vide** (juste l'en-tête)
- [ ] Onglet "Acquéreurs" avec les 5 lignes visibles
- [ ] Sim.ai ouvert — workflow "Matching Vendeur ↔ Acquéreurs" **activé**
- [ ] Gmail ouvert dans un onglet séparé — boîte de réception vide ou triée
- [ ] Données Mme Dubois prêtes à copier (voir ci-dessous)

## Données à saisir en live

Copier-coller cette ligne dans le Google Sheet "Mandats vendeurs" :

| Nom vendeur | Type | Localisation | Surface | Bouquet estimé | Rente estimée | Occupation | Description |
|---|---|---|---|---|---|---|---|
| Mme Dubois | Appartement T4 | Lyon 6e, rue des Lilas | 85 m² | 90 000 € | 800 €/mois | Occupé (DUH) | Bon état général, cuisine à refaire, 4e étage avec ascenseur, lumineux, proche transports et commerces |

## Script de la démo (~5 min)

**1. Montrer les acquéreurs** (30 sec)
> "Voici notre base de 5 acquéreurs. Chacun a ses critères : zone, budget, type de bien, et des préférences libres comme 'lumineux' ou 'proche commerces'."

**2. Montrer le workflow** (30 sec)
> "Notre workflow en 4 étapes : un mandat arrive → l'IA extrait les caractéristiques → elle croise avec nos acquéreurs → elle envoie un mail personnalisé à ceux qui matchent."

**3. Ajouter le mandat** (30 sec)
> "Un nouveau mandat arrive — Mme Dubois, un T4 à Lyon 6e. Je l'ajoute dans le tableau."
> *(Coller la ligne dans le Sheet)*

**4. Observer l'exécution** (1 min)
> "Le workflow se déclenche automatiquement. On peut voir les étapes s'exécuter dans Sim.ai."
> *(Montrer le workflow en cours d'exécution)*

**5. Montrer les emails** (2 min)
> "Basculons sur Gmail... Trois emails sont arrivés. Sophie, Jean et Alain. Pas Marc — il cherchait une maison à Aix. Pas Claire — elle cherchait à Paris."
> *(Ouvrir l'email de Sophie)*
> "Regardez : l'IA a mentionné que ce bien est lumineux et proche des transports — exactement ce que Sophie cherchait. Chaque email est unique."

**6. Conclure** (30 sec)
> "Le conseiller n'a rien fait d'autre qu'ajouter une ligne dans un tableau. Pas de code, pas de tri manuel, pas de copier-coller. L'IA fait le matching ET la personnalisation."

## Plan B

Si le workflow ne se déclenche pas :
1. Lancer manuellement le workflow dans Sim.ai (bouton "Run")
2. Si le LLM échoue : montrer les résultats du test J-1 (screenshots)
