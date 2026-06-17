# Simulateur Impôt PER et Placement

> Outil personnel de simulation fiscale et de stratégie d'épargne retraite pour foyer français.  
> Fichier HTML autonome — aucune installation, aucune dépendance, aucune donnée envoyée sur internet.

---

## ⚠️ Avertissement légal

Cet outil est fourni **à titre informatif et éducatif uniquement**. Il ne constitue pas un conseil fiscal, financier ou juridique. Les calculs sont des estimations basées sur le barème en vigueur à la date de mise à jour. Consultez un professionnel (conseiller fiscal, expert-comptable, CGP) avant toute décision patrimoniale.

L'auteur décline toute responsabilité en cas d'erreur de calcul ou d'utilisation inappropriée.

---

## Fonctionnalités

### Onglet 1 — Simulation fiscale
- Calcul de l'impôt sur le revenu du foyer (1 ou 2 déclarants)
- Prise en compte des pensions, retraits PER imposables, versements PER déductible, dons, crédits d'impôt
- Abattement 10% sur pensions (plancher et plafond automatiques)
- Mutualisation des plafonds PER entre conjoints (mode M3)
- Décote automatique (célibataire ou couple)
- **Taux marginal d'imposition (TMI)** affiché
- **Taux moyen effectif** affiché
- **Marge de sortie PER avant tranche 30%** — montant maximum à sortir du PER sans franchir la tranche supérieure
- **Versement PER pour devenir non imposable** — calculé par dichotomie, avec note sur les plafonds cumulés
- Plafond PER pré-rempli automatiquement depuis le PASS saisi dans l'onglet Paramètres

### Onglet 2 — Stratégie PER et placement
- Saisie des capitaux PER à rapatrier (2 PER possibles) avec année de sortie
- Objectif mensuel à compenser (perte de revenus à la retraite)
- **5 enveloppes activables/désactivables** : PEA principal, PEA épouse, CTO, Livrets, Assurance vie
- Pour chaque enveloppe : capital actuel, rendement, part du PER affectée, fiscalité
- Transfert annuel automatique livrets → PEA configurable
- Simulation sur **5 ans, 10 ans et 15 ans**
- Affichage des gains nets mensuels par enveloppe et du total
- **Capital CTO (Compte titre ordinaire) en évolution** année par année
- **Capital total patrimoine** en évolution
- PEA affiché 🔒 jusqu'à la date de déblocage (5 ans après ouverture)
- Synthèse fiscale : sortie totale vs sortie étalée à 11%
- Alerte si la somme des parts d'affectation ≠ 100%

### Onglet 3 — Paramètres annuels
- Barème IR entièrement modifiable (5 tranches)
- Paramètres de décote modifiables (seuils, constantes, coefficient)
- PASS modifiable avec calcul automatique du plafond PER
- Reports de plafond PER cumulés N-1/N-2/N-3 par déclarant
- Tableau de synthèse des plafonds disponibles par déclarant et total foyer
- Mise à jour annuelle en quelques minutes sans toucher au code

### Onglet 4 — Sources & historique
- Liens directs vers les sources officielles (economie.gouv.fr, service-public.fr, BOFiP, impots.gouv.fr)
- Historique des barèmes et paramètres de décote par année

---

## Utilisation

### Prérequis
Aucun. Le fichier fonctionne directement dans tout navigateur moderne (Chrome, Firefox, Edge, Safari).

### Démarrage rapide
1. Télécharger le fichier `simulateur_impot_PER_et_placement_V1.5.1.html`
2. Ouvrir dans votre navigateur (double-clic ou glisser-déposer)
3. Aller dans l'onglet **Paramètres annuels** → vérifier que le barème correspond à l'année en cours
4. Saisir le PASS de l'année N-1
5. Revenir dans l'onglet **Simulation** → saisir les revenus du foyer
6. Le simulateur calcule automatiquement impôt, TMI, marge PER et plafond de versement
7. Aller dans l'onglet **Stratégie PER** → saisir les capitaux PER et configurer les enveloppes
8. Cliquer **Calculer la stratégie** pour obtenir les projections sur 5/10/15 ans

### Mise à jour annuelle (novembre–février)
1. Aller dans l'onglet **Paramètres annuels**
2. Mettre à jour les seuils du barème IR (source : service-public.fr ou economie.gouv.fr)
3. Mettre à jour les paramètres de décote
4. Mettre à jour le PASS
5. Ajouter les nouvelles valeurs dans le tableau historique de l'onglet **Sources & historique**

---

## Valeurs par défaut

| Paramètre | Valeur | Source |
|-----------|--------|--------|
| Barème | 2026 (revenus 2025) | Loi de finances 2026 |
| Revalorisation | +0,9% | LFI 2026 |
| Tranche 0% | jusqu'à 11 600 € | LFI 2026 |
| Tranche 11% | jusqu'à 29 579 € | LFI 2026 |
| Tranche 30% | jusqu'à 84 577 € | LFI 2026 |
| Tranche 41% | jusqu'à 181 917 € | LFI 2026 |
| Seuil décote célibataire | 1 982 € | LFI 2026 |
| Constante décote célibataire | 897 € | LFI 2026 |
| Seuil décote couple | 3 277 € | LFI 2026 |
| Constante décote couple | 1 483 € | LFI 2026 |
| Coefficient décote | 0,4525 | LFI 2026 |
| PASS | 47 100 € | 2025 |

---

## Historique des versions

### V1.5.1 — Juin 2026
- Ajout footer disclaimer permanent visible sur tous les onglets
- Précision sur le bon usage (réflexion personnelle, pas un conseil MIF2)
- Mention explicite de la co-création avec Claude (Anthropic) et de la validation utilisateur
- Lien vers le dépôt GitHub et rappel de la licence MIT en pied de page

### V1.5 — Juin 2026
- Ajout onglet **Stratégie PER** avec simulation 5/10/15 ans
- 5 enveloppes activables : PEA principal, PEA épouse, CTO, Livrets, Assurance vie
- Capital CTO et capital total patrimoine en évolution année par année
- Calcul automatique du plafond PER depuis le PASS
- Champs reports plafond PER cumulés N-1/N-2/N-3
- Calcul par dichotomie du versement PER pour non-imposition
- Marge de sortie PER avant tranche 30% corrigée (bug index barème)

### V1.4 — Juin 2026
- Ajout onglet **Sources & historique** avec URLs officielles et tableau comparatif barèmes
- Fusion du fichier sources_parametres_annuels.txt dans le simulateur
- Mise à jour barème 2026 (revenus 2025, revalorisation +0,9%)

### V1.3 — Juin 2026
- Ajout TMI (taux marginal d'imposition) dans les résultats
- Ajout taux moyen effectif
- Ajout marge de sortie PER avant tranche 30%
- Ajout mention "(par part)" dans le détail par tranche

### V1.2 — Juin 2026
- Onglet **Paramètres annuels** — barème et décote entièrement modifiables sans toucher au code
- Barème dynamique lu depuis les champs de l'onglet Paramètres
- Décote dynamique

### V1.1 — Juin 2026
- Ajout déclarant 2 avec animation d'apparition
- Mutualisation des plafonds PER mode M3
- Dons à 66% et 75%, crédits d'impôt
- Abattement pensions avec plancher et plafond

### V1.0 — Juin 2026
- Version initiale : simulation IR foyer, barème progressif, décote, abattement pensions
- 1 déclarant, versements PER déductibles

---

## Structure du projet

```
simulateur-impot-per-placement/
├── simulateur_impot_PER_et_placement_V1.5.1.html   # Fichier principal
├── README.md                                         # Ce fichier
├── CHANGELOG.md                                      # Historique détaillé des versions
├── LICENSE                                           # Licence MIT
└── GUIDE_GITHUB.md                                   # Guide de publication et mise à jour
```

---

## Contribuer

Les suggestions d'amélioration sont les bienvenues via les Issues GitHub.  
Les Pull Requests peuvent être soumises pour correction de bugs ou ajout de fonctionnalités.

---

## Licence

Ce projet est distribué sous licence **MIT** — voir le fichier [LICENSE](LICENSE) pour le texte complet.  
Utilisation libre, y compris commerciale, avec mention de l'auteur.

---

## Sources officielles

| Source | URL |
|--------|-----|
| Barème IR | https://www.economie.gouv.fr/particuliers/impots-et-fiscalite/gerer-mon-impot-sur-le-revenu/comment-calculer-votre-impot-dapres-le-bareme-de-limpot-sur-le-revenu |
| Service-public.fr barème | https://www.service-public.fr/particuliers/actualites/A18045 |
| BOFiP | https://bofip.impots.gouv.fr/bofip/2412-PGP.html |
| Décote | https://www.economie.gouv.fr/particuliers/impots-et-fiscalite/gerer-mon-impot-sur-le-revenu/pouvez-vous-beneficier-de-la-decote-de-limpot-sur-le-revenu |
| Plafonds PER | https://www.service-public.fr/particuliers/vosdroits/F34982 |
| Simulateur officiel DGFiP | https://www.impots.gouv.fr/simulateurs-et-calculettes |
