#  Mini-projet Data Mining & BI — Prédiction des ventes d'un réseau de distribution multi-magasin

##  Description

Ce projet applique des techniques de **Data Mining**, de **Business Intelligence** et de **Machine Learning** pour analyser et prédire les ventes d'un réseau de distribution composé de plusieurs magasins. Il couvre l'intégralité du pipeline data : modélisation dimensionnelle, analyse exploratoire, visualisation interactive et prédiction par apprentissage automatique.

---

##  Architecture des données

Le projet exploite deux schémas dimensionnels :

- **Schéma en étoile** : `FACT_VENTES`, `DIM_PRODUIT`, `DIM_CLIENT`, `DIM_MAGASIN`, `DIM_EMPLOYE`, `DIM_PROMOTION`, `DIM_DATE`
- **Schéma en flocon** : `SNOW_FACT_VENTES` + dimensions hiérarchisées (année, semestre, trimestre, mois, semaine, date, catégorie, produit, client, magasin, employé, promotion)

---

##  Étapes du projet

### 1. Chargement & Nettoyage des données
- Lecture de 21 fichiers CSV
- Nettoyage des colonnes et gestion des valeurs manquantes
- Fusion des tables (jointures sur les clés dimensionnelles)

### 2. Analyse Exploratoire (EDA)
- Analyse des ventes par produit, magasin, client et période
- Visualisations avec **Matplotlib**, **Seaborn** et **Plotly**
- Identification des tendances temporelles et des KPIs métier

### 3. Modélisation Machine Learning
Trois modèles de régression ont été entraînés et comparés :

| Modèle               | R² Score   | MAE (€)  |
|----------------------|------------|----------|
| Régression Linéaire  | -1026.66   | 11.86    |
| Arbre de Décision    | **-56.69** | **3.84** |
| Forêt Aléatoire      | -143.95    | 6.09     |

>  **Meilleur modèle** : Arbre de Décision (MAE le plus faible)

---

##  Technologies utilisées

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-orange)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-ML-yellow)
![Plotly](https://img.shields.io/badge/Plotly-Interactive-purple)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF)

- **Python 3.12** — Pandas, NumPy, Scikit-learn
- **Visualisation** — Matplotlib, Seaborn, Plotly
- **Environnement** — Kaggle Notebook
- **BI** — Modélisation étoile & flocon (inspirée Power BI)

---

##  Structure du projet
