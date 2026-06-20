# Mode d'emploi — Simulateur Impôt PER et Placement

> Version 1.6 — Juin 2026

---

## À qui s'adresse cet outil ?

Ce simulateur est conçu pour toute personne souhaitant **optimiser fiscalement** son épargne retraite et comparer les stratégies de placement. Il couvre en particulier :

- Les **salariés** qui versent sur un PER et veulent savoir combien verser pour optimiser leur imposition
- Les **retraités ou futurs retraités** qui s'interrogent sur la meilleure façon de rapatrier leur PER (rente ou capital, étalé ou en une fois)
- Toute personne souhaitant comparer **PER vs PEA direct** ou **rente viagère vs capital placé**

Il gère les revenus suivants : salaires, pensions de retraite, retraits PER imposables, versements PER déductibles.

---

## Les 4 onglets

### Onglet 1 — Simulation fiscale

**Ce qu'il fait** : calcule votre impôt sur le revenu et affiche les indicateurs clés pour prendre des décisions fiscales.

**Comment l'utiliser** :

1. Cochez **"Couple"** si vous déclarez à deux — le déclarant 2 apparaît
2. Renseignez le **nombre de parts** (2 pour un couple sans enfant, 2,5 avec un enfant...)
3. Pour chaque déclarant, saisissez :
   - **Salaires** : montant annuel brut — l'abattement 10% est calculé automatiquement (plancher 495 €, plafond 14 171 €). Si vous optez pour les frais réels, cochez la case et saisissez le montant exact
   - **Pensions** : montant pré-rempli de votre déclaration (déjà net de CSG déductible) — l'abattement 10% pensions est calculé automatiquement (plancher 442 €, plafond 4 321 €)
   - **Retraits PER imposables** : si vous avez sorti des sommes de votre PER cette année
   - **Plafond PER** : pré-rempli automatiquement depuis le PASS (onglet Paramètres). Ajustez avec vos reports si vous avez des plafonds non utilisés des années précédentes
   - **Versement PER** : ce que vous versez cette année sur votre PER
4. Renseignez les **dons** (66% ou 75%) et **crédits d'impôt** si applicable
5. Cliquez **"Calculer"**

**Ce que vous voyez dans les résultats** :
- Détail du calcul par tranche (par part)
- Impôt brut, décote, réductions, impôt net
- **TMI** (Taux Marginal d'Imposition) — le taux qui s'applique au dernier euro gagné. Clé pour décider si un versement PER ou une sortie PER est avantageux
- **Taux moyen effectif** — ce que vous payez réellement en proportion de vos revenus
- **Marge de sortie PER avant tranche 30%** — montant maximum que vous pouvez sortir du PER cette année sans franchir la tranche supérieure *(en vert)*
- **Versement PER pour devenir non imposable** — montant exact à verser pour ramener l'impôt à 0 €, calculé par dichotomie *(en violet)*. ⚠️ Si vous avez des reports de plafonds, votre vrai plafond disponible figure sur votre avis d'imposition (page 2, case "Plafond épargne retraite disponible")

---

### Onglet 2 — Stratégie PER

**Ce qu'il fait** : simule le rapatriement de vos PER dans vos enveloppes de placement (PEA 1, PEA 2, CTO) et projette les revenus générés sur 5, 10 et 15 ans.

**Prérequis** : avoir renseigné vos revenus dans l'onglet Simulation (la marge à 11% est reprise automatiquement).

**Comment l'utiliser** :

1. **Capitaux PER à rapatrier** :
   - Saisissez le capital brut de chaque PER et l'année de sortie prévue
   - Renseignez votre **objectif mensuel** à compenser (ex : perte de salaire à la retraite). Mettez 0 si vous ne voulez pas d'objectif fixe
   - Saisissez l'**année de début de simulation** (ex : 2026 pour voir dès maintenant)
   - Choisissez le **mode de sortie** :
     - *Sortie étalée à 11% (réaliste)* : le code sort chaque année exactement la marge disponible avant la tranche 30%, et verse le capital net progressivement dans les enveloppes
     - *Sortie totale en 1 an (TMI 30%)* : tout est sorti en une seule fois, à titre de comparaison pour voir le coût fiscal

2. **Enveloppes de placement** :
   - Activez/désactivez chaque enveloppe (PEA 1, PEA 2, CTO) avec la case à cocher
   - Pour chaque PEA : saisissez le capital actuel, l'**année ET le mois d'ouverture** (important pour le calcul précis du déblocage à 5 ans), le rendement attendu (%), et la part (%) du capital PER à y affecter
   - Pour le CTO : capital actuel, rendement, part PER, et fiscalité (PFU 30% ou barème 11%)
   - ⚠️ La somme des parts PEA 1 + PEA 2 + CTO doit faire **100%**

3. Cliquez **"Calculer la stratégie"**

**Ce que vous voyez dans les résultats** :

- **Synthèse fiscale** : comparaison de l'impôt entre sortie totale (TMI 30%) et sortie étalée (11%), avec la marge annuelle disponible
- **Répartition cible** : combien arrive dans chaque enveloppe au total, à terme
- **Tableaux de simulation sur 5, 10 et 15 ans** avec pour chaque année :
  - Capital PEA 1, PEA 2, CTO (🔒 tant que non débloqué)
  - Gains CTO/mois : disponibles immédiatement, retirés chaque année
  - Gains PEA/mois : en *italique gris* avec le potentiel capitalisé avant déblocage, puis en bleu une fois disponibles
  - Plus-value cumulée : richesse réelle créée depuis le départ (capital final + gains CTO encaissés - capital investi)
  - Total/mois disponible : ce que vous pouvez réellement retirer
  - Capital total de toutes les enveloppes

**Règles appliquées** :
- Le CTO retire ses gains chaque année sans délai (pas de blocage légal)
- Les PEA capitalisent leurs gains jusqu'au déblocage (5 ans après le mois d'ouverture)
- Les versements PER ne démarrent qu'à partir de l'année de sortie choisie

---

### Onglet 3 — Comparateurs

**Ce qu'il fait** : répond aux deux grandes questions stratégiques sur le PER.

#### Comparateur 1 — Rente viagère vs capital placé

Renseignez :
- Le **capital concerné** par la rente (ex : 50 000 €)
- La **rente annuelle proposée** par votre assureur (ex : 2 345 €/an)
- L'**âge actuel** du titulaire et son **espérance de vie restante** (estimée)
- Le **rendement de référence** de vos placements (ex : 6% ou 7%/an)

Le simulateur calcule :
- Le **rendement implicite** de la rente (rente ÷ capital) — en rouge si inférieur à votre rendement de référence
- Le **point mort** : année où la rente cumulée dépasse les gains du capital placé
- Un **tableau comparatif** année par année sur l'espérance de vie
- Le **capital transmissible** à vos héritiers : 0 € avec la rente, capital + gains avec l'option capital

⚠️ Calcul simplifié : ne tient pas compte de la fiscalité de la rente (abattement 10% puis barème IR) ni de celle du capital (PS 17,2% sur PEA, PFU sur CTO).

#### Comparateur 2 — PER vs placement direct (PEA/CTO)

Renseignez :
- Le **versement annuel** envisagé sur le PER
- Le **TMI à l'entrée** (au moment du versement) et **à la sortie** (à la retraite)
- La **durée de détention** avant sortie (en années)
- Le **rendement annuel** du placement
- La **fiscalité de sortie alternative** (PEA PS 17,2%, CTO PFU 30%, ou barème 11%)

Le simulateur compare sur un seul versement :
- **Scénario A (avec PER)** : versement brut → fructification → sortie taxée au TMI de sortie
- **Scénario B (sans PER, placement direct)** : versement net (après impôt non économisé) → fructification → sortie taxée selon la fiscalité alternative

⚠️ Calcul simplifié : suppose un seul versement et une seule sortie. Pour des versements annuels répétés sur plusieurs décennies, l'avantage du PER est encore plus marqué.

---

### Onglet 4 — Paramètres annuels

**Ce qu'il fait** : permet de mettre à jour les valeurs fiscales chaque année sans toucher au code.

**À mettre à jour chaque automne/hiver** (après la loi de finances) :
- Les **5 tranches du barème IR**
- Les **paramètres de décote** (seuils, constantes, coefficient)
- Le **PASS** (Plafond Annuel de la Sécurité Sociale) de l'année N-1
- Les **reports de plafond PER** non utilisés par déclarant (N-1, N-2, N-3 cumulés — montant total sur votre avis d'imposition)

Sources officielles : voir l'onglet **Sources & historique** pour les URLs exactes.

---

## Mise à jour annuelle (5 minutes)

1. Aller dans l'onglet **Paramètres annuels**
2. Mettre à jour les seuils du barème IR
3. Mettre à jour les paramètres de décote
4. Mettre à jour le PASS
5. Vérifier les reports de plafond PER sur votre avis d'imposition

---

## Limites du simulateur

- Ne gère pas les revenus fonciers, BIC, BNC, dividendes, plus-values de cession
- Ne gère pas la CEHR (contribution exceptionnelle sur les hauts revenus)
- Le comparateur PER vs PEA direct suppose un seul versement (pas des versements répétés)
- Le comparateur rente vs capital ne tient pas compte de la fiscalité de la rente ni du capital
- Les rendements sont des hypothèses — les résultats réels dépendront des marchés

---

## Avertissement légal

Cet outil est fourni à titre informatif et éducatif uniquement. Il ne constitue pas un conseil fiscal, financier ou juridique. Vérifiez vos résultats sur [impots.gouv.fr](https://www.impots.gouv.fr/simulateurs-et-calculettes) avant toute décision.

Licence MIT — Projet open source — [github.com/J34NMY/simulateur-impot-per-placement](https://github.com/J34NMY/simulateur-impot-per-placement)
