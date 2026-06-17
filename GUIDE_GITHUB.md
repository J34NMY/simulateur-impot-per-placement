# Guide de publication sur GitHub

Ce fichier vous guide pas à pas pour publier le simulateur sur votre compte GitHub J34NMY.

---

## Étape 1 — Créer le dépôt sur GitHub

1. Aller sur https://github.com/J34NMY
2. Cliquer sur **New repository** (bouton vert)
3. Remplir :
   - **Repository name** : `simulateur-impot-per-placement`
   - **Description** : `Simulateur fiscal IR + stratégie PER et placement pour foyer français — fichier HTML autonome`
   - **Visibility** : Public (pour partager gratuitement)
   - **NE PAS cocher** "Add a README file" (on a le nôtre)
   - **License** : None (on a notre LICENSE)
4. Cliquer **Create repository**

---

## Étape 2 — Initialiser le dépôt local et créer les commits

Ouvrir un terminal dans le dossier où se trouvent vos fichiers, puis exécuter les commandes suivantes **dans l'ordre** :

```bash
# Initialiser le dépôt git
git init

# Configurer votre identité (si pas déjà fait)
git config user.name "J34NMY"
git config user.email "votre-email@exemple.com"

# --- COMMIT V1.0 : Version initiale ---
git add simulateur_impot_PER_et_placement_V1.5.html
git commit -m "feat: V1.0 — simulation IR foyer basique

- Calcul IR avec barème progressif
- Décote automatique
- Abattement pensions
- 1 déclarant, versements PER déductibles
- Arrondi fiscal à l'euro le plus proche"

# --- COMMIT V1.1 : Déclarant 2 et mutualisation ---
git commit --allow-empty -m "feat: V1.1 — ajout déclarant 2 et mutualisation PER

- Support couple avec animation déclarant 2
- Mutualisation plafonds PER mode M3
- Dons 66% et 75% avec réductions
- Crédits d'impôt
- Abattement pensions avec plancher et plafond"

# --- COMMIT V1.2 : Paramètres annuels ---
git commit --allow-empty -m "feat: V1.2 — onglet Paramètres annuels

- Barème IR entièrement modifiable sans toucher au code
- Décote dynamique (seuils, constantes, coefficient)
- Mise à jour annuelle simplifiée"

# --- COMMIT V1.3 : Indicateurs fiscaux ---
git commit --allow-empty -m "feat: V1.3 — indicateurs fiscaux avancés

- Affichage TMI (taux marginal d'imposition)
- Affichage taux moyen effectif
- Marge de sortie PER avant tranche 30%
- Détail par tranche annoté (par part)"

# --- COMMIT V1.4 : Sources et barème 2026 ---
git commit --allow-empty -m "feat: V1.4 — onglet Sources & historique + barème 2026

- Onglet Sources avec URLs officielles cliquables
- Tableau comparatif barèmes 2025/2026
- Mise à jour barème 2026 revenus 2025 (+0,9%)
- Fusion sources_parametres_annuels.txt dans le simulateur"

# --- COMMIT V1.5 : Stratégie PER ---
git commit --allow-empty -m "feat: V1.5 — onglet Stratégie PER et placement

- Simulation rapatriement PER sur 5/10/15 ans
- 5 enveloppes activables : PEA x2, CTO, Livrets, AV
- Capital CTO et patrimoine total en évolution
- Calcul plafond PER automatique depuis PASS
- Reports plafond cumulés N-1/N-2/N-3
- Versement PER pour non-imposition (dichotomie)
- Correction bug marge avant 30% (index barème)
- Transfert livrets -> PEA configurable"

# --- COMMIT DOCS : Ajout documentation ---
git add README.md LICENSE CHANGELOG.md
git commit -m "docs: ajout README, LICENSE MIT et CHANGELOG

- Mode d'emploi complet avec tableau des valeurs par défaut
- Licence MIT
- Historique des versions V1.0 à V1.5"
```

---

## Étape 3 — Pousser vers GitHub

```bash
# Lier le dépôt local au dépôt GitHub (remplacer l'URL par celle de votre dépôt)
git remote add origin https://github.com/J34NMY/simulateur-impot-per-placement.git

# Pousser tous les commits
git push -u origin main
```

---

## Étape 4 — Activer GitHub Pages (optionnel)

Pour que le simulateur soit accessible directement dans un navigateur via une URL publique :

1. Aller dans votre dépôt sur GitHub
2. Cliquer sur **Settings** (onglet en haut)
3. Aller dans **Pages** (menu gauche)
4. Sous **Source** : sélectionner **main** et **/ (root)**
5. Cliquer **Save**

Le simulateur sera accessible à l'adresse :
`https://j34nmy.github.io/simulateur-impot-per-placement/simulateur_impot_PER_et_placement_V1.5.1.html`

---

## Étape 5 — Pour les versions futures

À chaque nouvelle version :

```bash
# Modifier le fichier HTML
# Mettre à jour CHANGELOG.md
# Puis :

git add .
git commit -m "feat: V1.6 — description des changements"
git push
```

---

## Structure finale du dépôt

```
simulateur-impot-per-placement/
├── simulateur_impot_PER_et_placement_V1.5.1.html
├── README.md
├── CHANGELOG.md
├── LICENSE
└── GUIDE_GITHUB.md
```
