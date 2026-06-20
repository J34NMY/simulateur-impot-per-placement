# Changelog

Toutes les modifications notables de ce projet sont documentées dans ce fichier.

Format basé sur [Keep a Changelog](https://keepachangelog.com/fr/1.0.0/).

---

## [1.6] — 2026-06-20

### Ajouté
- Onglet **Comparateurs** séparé avec deux modules indépendants
- **Comparateur 1 — Rente viagère vs capital placé** : calcul du rendement implicite de la rente, point mort, évolution comparée sur l'espérance de vie, capital transmissible
- **Comparateur 2 — PER vs placement direct (PEA/CTO)** : comparaison nette après fiscalité, verdict contextuel selon TMI entrée/sortie
- Onglet **Stratégie PER** entièrement refondu :
  - 3 enveloppes : PEA 1, PEA 2, CTO (Livrets et AV supprimés pour simplifier)
  - Champ "Année de début de simulation" paramétrable (défaut 2026)
  - Champ "Mois d'ouverture" pour chaque PEA (précision du déblocage au mois près)
  - Mode de sortie PER : étalé à 11% ou one-shot (TMI 30%) au choix
  - Versements PER conditionnés à l'année de sortie réelle (pas avant 2028 si c'est la date choisie)
  - CTO disponible immédiatement sans blocage artificiel, gains retirés chaque année
  - PEA capitalisent jusqu'au déblocage, gains disponibles après 5 ans
  - Colonne "Gains CTO/mois" (disponibles immédiatement)
  - Colonne "Gains PEA/mois" avec potentiel affiché même pendant le blocage
  - Colonne "Plus-value cumulée" = capital total + gains CTO encaissés - capital investi
  - Objectif mensuel à 0 par défaut (paramétrable)
- Onglet **Simulation** : ajout des salaires par déclarant avec abattement 10% automatique (plancher 495 €, plafond 14 171 €) et option frais réels
- Calcul du plafond PER automatique depuis le PASS avec reports cumulés N-1/N-2/N-3

### Corrigé
- Capital affiché en fin d'année (après gains) et non en début d'année
- Versements PER démarrent bien à l'année de sortie choisie, pas avant
- Capital net de référence cohérent avec le mode de sortie choisi (étalé → capitalNet11, one-shot → capitalNet)
- Plus-value cumulée remplace les "intérêts cumulés" qui n'avaient pas de signification financière réelle

### Renommé
- PEA principal / PEA épouse → PEA 1 / PEA 2 (libellés neutres)
- Fichier : `simulateur_impot_PER_et_placement_V1.5.1.html` → `simulateur_impot_PER_et_placement_V1.6.html`

---

## [1.5.1] — 2026-06-10

### Ajouté
- Footer disclaimer permanent visible en bas de page sur tous les onglets
- Bloc "Avertissement" avec lien vers le simulateur officiel DGFiP
- Bloc "Bon usage" précisant les cas d'utilisation légitimes
- Bloc "Co-création" mentionnant la collaboration avec Claude (Anthropic)
- Lien vers le dépôt GitHub et rappel de la licence MIT en pied de page

### Renommé
- `simulateur_impot_PER_et_placement_V1.5.html` → `simulateur_impot_PER_et_placement_V1.5.1.html`

---

## [1.5] — 2026-06-10

### Ajouté
- Onglet **Stratégie PER** : simulation du rapatriement des PER sur 5/10/15 ans
- 5 enveloppes activables/désactivables : PEA principal, PEA épouse, CTO, Livrets, Assurance vie
- Calcul automatique du plafond PER depuis le PASS
- Calcul par dichotomie du versement PER exact pour devenir non imposable
- Synthèse fiscale : comparaison sortie totale (TMI 30%) vs sortie étalée (11%)

### Corrigé
- Bug index barème dans le calcul de la marge avant tranche 30% (bareme[2] → bareme[1])

---

## [1.4] — 2026-06-10

### Ajouté
- Onglet **Sources & historique** avec URLs officielles et tableau comparatif barèmes
- Mise à jour barème 2026 (revenus 2025, revalorisation +0,9%)

---

## [1.3] — 2026-06-10

### Ajouté
- TMI, taux moyen effectif, marge de sortie PER avant tranche 30%

---

## [1.2] — 2026-06-10

### Ajouté
- Onglet **Paramètres annuels** : barème IR et décote entièrement modifiables

---

## [1.1] — 2026-06-10

### Ajouté
- Déclarant 2, mutualisation PER mode M3, dons, crédits d'impôt

---

## [1.0] — 2026-06-10

### Ajouté
- Version initiale : calcul IR foyer, barème progressif, décote, abattement pensions
