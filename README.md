Ce projet est une analyse approfondie d'un jeu de données sur les pourboires dans un restaurant, utilisant Python et ses bibliothèques d'analyse de données.

#
## requirements

- Python 3.13.1
- Pandas
- NumPy
- Seaborn
- Matplotlib
- SciPy

##  Installation

1. Clonez ce dépôt :
```bash
git clone [https://github.com/nguekeuarthur/TpData.git]
```

2. Installez les dépendances requises :
```bash
pip install -r requirements.txt
```

##  Fonctionnalités

L'analyse comprend :

1. **Exploration des données**
   - Aperçu des données
   - Types de données
   - Statistiques descriptives
   - Détection des valeurs manquantes
     ```python
     # Recherche de valeurs manquantes
     # -----------------------------
     # .isnull() crée un DataFrame booléen (True si valeur manquante, False sinon)
     # .sum() additionne les True par colonne (True = 1), donc on obtient le nombre de NaN par colonne
     print(tips.isnull().sum())
     ```

2. **Visualisations**
   - Histogrammes des additions et pourboires
   - Boîtes à moustaches par jour
   - Nuages de points (scatterplots)
   - Graphiques de corrélation

3. **Analyses statistiques**
   - Corrélations linéaires
   - Tests statistiques
   - Analyses par groupes
   - Comparaisons de moyennes

4. **Manipulation de données**
   - Calculs vectorisés avec NumPy
   - Filtrage conditionnel
   - Agrégations et groupements
   - Transformations de données

##  Analyses et Résultats Détaillés

### 1. Analyse des Valeurs Manquantes
Pour identifier les valeurs manquantes, j'ai utilise la combinaison `isnull().sum()`. La fonction `isnull()` retourne True pour chaque cellule vide, et `sum()` additionne ces True (où True = 1) pour obtenir le nombre de valeurs manquantes.

### 2. Distribution des Données
Les histogrammes montrent que :
- La plupart des additions se situent entre 10 et 20 dollars
- Les pourboires sont majoritairement entre 2 et 4 dollars

### 3. Analyse des Fumeurs
- Le jeu de données contient environ 38% de fumeurs
- La répartition est équilibrée entre hommes et femmes

### 4. Analyse par Jour
- Les jours avec la plus grande variabilité de pourboires sont samedi et dimanche
- Vendredi présente la répartition la plus stable
- Le dimanche présente la plus grande variabilité en termes de pourcentage de pourboire

### 5. Corrélations et Relations
- **Total Bill vs Tip** : Corrélation positive significative (r ≈ 0.67)
- **Size vs Tip** : Corrélation positive plus faible (r ≈ 0.489)
- Les pourboires augmentent avec le montant de l'addition et le nombre de personnes

### 6. Comparaison Fumeurs vs Non-fumeurs
- Non-fumeurs : moyenne de 2.99$ de pourboire
- Fumeurs : moyenne de 3.00$ de pourboire
- La différence n'est pas statistiquement significative

### 7. Analyse des Grandes Tables
- Pour les tables de 4 personnes ou plus
- Pourboire moyen : environ 4.22$

### 8. Pourboires Exceptionnels
- 39 cas où le pourboire représente plus de 20% de l'addition

### 9. Manipulation des Données
- Conversion en NumPy : tableau de forme (244, 2)
- Concaténation des données hommes/femmes : index non conservé après concaténation

##  Structure du Projet

```
.
├── README.md
├── analysis.ipynb      # Notebook de travail
└── requirements.txt   # Dépendances du projet
```

##  Utilisation

1. Ouvrez le notebook `analysis.ipynb` dans Jupyter Notebook ou JupyterLab
2. Exécutez les cellules dans l'ordre pour reproduire l'analyse

