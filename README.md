# Optimisation du portefeuille de PolyFinances sous contrainte

Ce projet présente une analyse détaillée et une optimisation du portefeuille de PolyFinances en utilisant diverses stratégies d'investissement et méthodes d'optimisation.

![image](https://github.com/user-attachments/assets/4d5a5dc5-87da-48c3-a303-42c88aa32c5d)

---

## ℹ️ Qu'est-ce que PolyFinances ?

[**PolyFinances**](https://www.polyfinances.ca/) est un parcours de spécialisation en finance à Polytechnique Montréal. Il regroupe des étudiants passionnés par les marchés financiers, l'investissement et la gestion de portefeuille. Les membres gèrent un portefeuille d'investissement de plus de 100 000 $ et participent à des activités telles que l'analyse financière, la gestion de portefeuille, les partenariats avec l'industrie et l'organisation d'événements comme le Datathon annuel et la Semaine PolyFinances.

---

## 📌 Description du projet

Ce projet vise à analyser et optimiser un portefeuille d'actions et d'ETFs en utilisant différentes stratégies d'allocation d'actifs sous contraintes.  

L'analyse comprend :

- L'évaluation de la performance historique
- L’optimisation du portefeuille selon différents critères :
  - Volatilité minimale
  - Ratio de Sharpe maximal
  - Expected Shortfall (5%)
- La comparaison des performances des portefeuilles optimisés sur un échantillon de test

---

## 📂 Contenu du répertoire

Ce répertoire contient les fichiers suivants :

| Fichier                                      | Description                                      |
|---------------------------------------------|--------------------------------------------------|
| [`Graphiques_Optimisation_sc_PolyFinances.zip`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/Graphiques_Optimisation_sc_PolyFinances.zip) | Archive contenant les graphiques générés         |
| [`Optimisation_sc_PolyFinances.ipynb`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/Optimisation_sc_PolyFinances.ipynb)        | Notebook d'analyse et d'optimisation   |
| [`Rapport_Optimisation_sc_PolyFinances.docx`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/Rapport_Optimisation_sc_PolyFinances.docx) | Rapport détaillé du projet             |
| [`portfolio_history_complete.xlsx`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/portfolio_history_complete.xlsx)           | Données historiques du portefeuille de PolyFinances             |

---

## ⚙️ Prérequis

Pour exécuter le [notebook](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/Optimisation_sc_PolyFinances.ipynb), vous aurez besoin des éléments suivants :

- [Google Colab](https://colab.research.google.com/) (recommandé) ou Jupyter Notebook
- Fichier de données : [`portfolio_history_complete.xlsx`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/portfolio_history_complete.xlsx)

---

## 📚 Librairies utilisées dans le projet d'optimisation de portefeuille

Le projet utilise les librairies Python suivantes pour l'analyse financière et l'optimisation de portefeuille :

### 📊 Visualisation, calculs et analyse de données

- [`matplotlib`](https://matplotlib.org/)
- [`numpy`](https://numpy.org/)
- [`pandas`](https://pandas.pydata.org/)
- [`seaborn`](https://seaborn.pydata.org/)

### 💹 Finance quantitative

- [`pypfopt`](https://pyportfolioopt.readthedocs.io/en/latest/)
- [`quantstats`](https://github.com/ranaroussi/quantstats)
- [`scipy.optimize`](https://docs.scipy.org/doc/scipy/reference/optimize.html)
- [`yfinance`](https://pypi.org/project/yfinance/)

---

## 📁 Structure du projet

Le notebook est organisé en plusieurs sections :

### 🔧 Préparation des données
- Importation des données historiques du portefeuille
- Téléchargement des prix ajustés depuis Yahoo Finance
- Organisation des données par secteur

### 🔢 Analyse du portefeuille actuel
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
- Analyse sectorielle des portefeuilles (Aggrégation des données par secteur)

---

## 📈 Résultats

Le notebook génère plusieurs visualisations, enregistrées dans le dossier `figures/`, notamment :

- Corrélation entre les secteurs
- Évolution de la valeur du portefeuille
- Distribution des rendements mensuels
- Drawdown du portefeuille
- Répartition des poids par stratégie
- Comparaison des performances des portefeuilles

Il est également possible de retrouver l'ensemble des graphiques dans le fichier [`Graphiques_Optimisation_sc_PolyFinances.zip`](https://github.com/rayanajakane/Optimisation-Portefeuille-PolyFinances/blob/main/Graphiques_Optimisation_sc_PolyFinances.zip).

En voici quelques exemples:

### Analyse du portefeuille de PolyFinances
![image](https://github.com/user-attachments/assets/b7e2d5f7-0d96-4ee7-8086-aa0c90a03c64)
![image](https://github.com/user-attachments/assets/93207931-27e0-4bed-a0ca-9cd22167e02b)

### Optimisation de portefeuille
![image](https://github.com/user-attachments/assets/7758f111-206e-45f5-9d6f-c367dcda1a3c)

### Tests des portefeuilles optimisés
![image](https://github.com/user-attachments/assets/239e9d00-f3bd-456c-8755-47a603a914cd)
![image](https://github.com/user-attachments/assets/55442719-a522-4809-a5c7-04aa312f544a)

---

## 👨‍🏫 Auteurs

Ce projet a été réalisé principalement par Rayan Ajakane, en collaboration avec Yasmine Aouinat pour l'analyse du portefeuille ainsi que Fedwa Bouya et Khai Nguyen pour la rédaction du rapport.

---
