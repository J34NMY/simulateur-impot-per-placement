# Changelog

Toutes les modifications notables de ce projet sont documentées dans ce fichier.

Format basé sur [Keep a Changelog](https://keepachangelog.com/fr/1.0.0/).

---

## [1.5] — 2026-06-10

### Ajouté
- Onglet **Stratégie PER** : simulation du rapatriement des PER sur 5/10/15 ans
- 5 enveloppes de placement activables/désactivables : PEA principal, PEA épouse, CTO, Livrets, Assurance vie
- Affichage du capital CTO en évolution année par année (capitalisation)
- Affichage du capital total patrimoine en évolution sur toute la période
- Calcul automatique du plafond PER depuis le PASS (onglet Paramètres)
- Champs de report plafond PER cumulé N-1/N-2/N-3 par déclarant
- Calcul par dichotomie du versement PER exact pour devenir non imposable
- Avertissement si la somme des parts d'affectation PER ≠ 100%
- Transfert annuel livrets → PEA configurable
- PEA affiché 🔒 avant la date de déblocage (5 ans après ouverture)
- Synthèse fiscale : comparaison sortie totale (TMI 30%) vs sortie étalée (11%)

### Corrigé
- Bug index barème dans le calcul de la marge avant tranche 30% (bareme[2] → bareme[1])

---

## [1.4] — 2026-06-10

### Ajouté
- Onglet **Sources & historique** : URLs officielles cliquables et tableau comparatif barèmes 2025/2026
- Fusion du fichier sources_parametres_annuels.txt dans le simulateur (un seul fichier)
- Mise à jour barème 2026 (revenus 2025) : revalorisation +0,9%
- Mention de la version et du barème en vigueur sous le titre

### Modifié
- Fonction showTab mise à jour pour gérer 3 onglets (+ sources)

---

## [1.3] — 2026-06-10

### Ajouté
- **TMI** (Taux Marginal d'Imposition) affiché dans les résultats avec note explicative
- **Taux moyen effectif** affiché dans les résultats
- **Marge de sortie PER avant tranche 30%** : montant foyer disponible à 11%
- Mention "(par part)" dans le titre "Détail par tranche"

---

## [1.2] — 2026-06-10

### Ajouté
- Onglet **Paramètres annuels** : barème IR et décote entièrement modifiables
- Barème dynamique lu depuis les champs de l'onglet (plus besoin de modifier le code)
- Décote dynamique (seuils, constantes, coefficient modifiables)

### Modifié
- Séparation logique calcul / paramètres pour faciliter la mise à jour annuelle

---

## [1.1] — 2026-06-10

### Ajouté
- Support du **déclarant 2** avec animation d'apparition/disparition
- **Mutualisation des plafonds PER** entre conjoints (mode M3 avec priorité plafond restant)
- Dons à 66% et 75% avec réductions automatiques
- Crédits d'impôt
- Abattement pensions avec plancher (442 €) et plafond (4 321 €)

---

## [1.0] — 2026-06-10

### Ajouté
- Version initiale du simulateur
- Calcul IR foyer : barème progressif, décote, abattement pensions
- 1 déclarant, versements PER déductibles avec plafond
- Arrondi fiscal à l'euro le plus proche
