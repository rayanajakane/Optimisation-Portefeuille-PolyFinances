# Optimisation du portefeuille de PolyFinances sous contrainte

Ce projet présente une analyse détaillée et une optimisation du portefeuille de PolyFinances en utilisant diverses stratégies d'investissement et méthodes d'optimisation.

---

## ℹ️ Qu'est-ce que PolyFinances ?

[**PolyFinances**](https://www.polyfinances.ca/) est un parcours de spécialisation en finance à Polytechnique Montréal. Il regroupe des étudiants passionnés par les marchés financiers, l'investissement et la gestion de portefeuille. Les membres gèrent un portefeuille d'investissement de plus de 100 000 $ et participent à des activités telles que l'analyse financière, la gestion de portefeuille, les partenariats avec l'industrie et l'organisation d'événements comme le Datathon annuel et la Semaine PolyFinances.

---

## 📌 Description du projet

Ce projet vise à analyser et optimiser un portefeuille d'actions en utilisant différentes stratégies d'allocation d'actifs sous contraintes.  
L'analyse comprend :

- L'évaluation de la performance historique
- L’optimisation du portefeuille selon différents critères :
  - Volatilité minimale
  - Ratio de Sharpe maximal
  - Expected Shortfall (5%)
- La comparaison des performances des portefeuilles optimisés sur un échantillon de test

---

## ⚙️ Prérequis

Pour exécuter ce notebook, vous aurez besoin des éléments suivants :

- [Google Colab](https://colab.research.google.com/) (recommandé) ou Jupyter Notebook
- Fichier de données : `portfolio_history_complete.xlsx`

### 📦 Installation des librairies nécessaires

Exécutez les cellules suivantes dans le notebook :

```python
!pip install quantstats
!pip install PyPortfolioOpt
!pip install yfinance
```

---

## 📁 Structure du projet

Le notebook est organisé en plusieurs sections :

### 🔧 Préparation des données
- Importation des données historiques du portefeuille
- Téléchargement des prix ajustés depuis Yahoo Finance
- Organisation des données par secteur

### 📊 Analyse du portefeuille actuel
- Analyse des rendements sectoriels et globaux
- Visualisations de la performance du portefeuille
- Analyse des corrélations entre secteurs

### 🔍 Optimisation du portefeuille
- **Ptf1** : Portefeuille à variance minimale (Poids ≥ 0)
- **Ptf2** : Variance minimale avec contraintes (2% ≤ Poids ≤ 15%)
- **Ptf3** : Maximisation du ratio rendement/risque (Poids ≥ 0)
- **Ptf4** : Maximisation du ratio rendement/risque avec contraintes (2% ≤ Poids ≤ 15%)
- **Ptf5** : Portefeuille équipondéré
- **Ptf6** : Minimisation de l’Expected Shortfall (5% pires cas)

### 🧪 Test des portefeuilles optimisés
- Comparaison des rendements des différents portefeuilles
- Analyse des métriques de performance :
  - Rendement annuel moyen
  - Volatilité
  - Ratio rendement/risque
  - Maximum drawdown
- Analyse sectorielle des portefeuilles

---

## 📈 Résultats

Le notebook génère plusieurs visualisations, enregistrées dans le dossier `figures/`, notamment :

- Corrélation entre les secteurs
- Évolution de la valeur du portefeuille
- Distribution des rendements mensuels
- Drawdown du portefeuille
- Répartition des poids par stratégie
- Comparaison des performances des portefeuilles

---

## 👨‍🏫 Auteurs

Ce projet a été réalisé principalement par Rayan Ajakane, en collaboration avec Yasmine Aouinat pour l'analyse du portefeuille ainsi que Fedwa Bouya et Khai Nguyen pour la rédaction du rapport.

---
