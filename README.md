# Analyse des ventes Superstore

Projet d'analyse exploratoire des ventes et des profits du jeu de données **Sample - Superstore**, réalisé avec Python et Jupyter Notebook.

Le notebook étudie la qualité des données, les indicateurs de performance, les ventes par catégorie et par segment, les tendances temporelles, ainsi que la relation entre remises, ventes et profits.

## Aperçu

La base locale contient **9 994 lignes** et **21 colonnes**, couvrant des commandes du **3 janvier 2014 au 30 décembre 2017**.

| Indicateur | Résultat |
|---|---:|
| Chiffre d'affaires | 2 297 200,86 $ |
| Profit total | 286 397,02 $ |
| Marge bénéficiaire globale | 12,47 % |
| Commandes uniques | 5 009 |
| Clients uniques | 793 |

Principaux résultats descriptifs :

- La catégorie **Technology** réalise le plus grand chiffre d'affaires (**836 154,03 $**) et le plus grand profit (**145 454,95 $**).
- La région **West** est la plus rentable, avec **108 418,45 $** de profit.
- Le segment **Consumer** représente le plus gros volume de ventes.
- **1 871 lignes** présentent un profit négatif.
- Aucune valeur manquante ni ligne strictement dupliquée n'est présente dans le fichier.

Ces chiffres proviennent uniquement de l'analyse exploratoire du fichier fourni et ne constituent pas une étude causale.

## Analyses réalisées

- Inspection de la structure, des types de données et de la qualité du jeu de données.
- Conversion des dates de commande et d'expédition au format `datetime`.
- Calcul des indicateurs clés : ventes, profits, quantité, marges, commandes et clients.
- Comparaison des ventes et profits par catégorie, sous-catégorie, région et segment.
- Identification des meilleurs produits par ventes et des produits les moins rentables.
- Analyse descriptive des ventes et marges selon le taux de remise.
- Étude des ventes et profits par année et par mois.
- Mesure des corrélations entre ventes, profits, quantités et remises.

## Visualisations

Le notebook génère les graphiques suivants dans `visualization/` :

| Graphique | Aperçu |
|---|---|
| Ventes par catégorie | [sales_by_category.png](visualization/sales_by_category.png) |
| Évolution mensuelle des ventes | [monthly_sales_revenue.png](visualization/monthly_sales_revenue.png) |
| Profit par région | [profit_by_region.png](visualization/profit_by_region.png) |
| Ventes par segment client | [sales_by_customer_segment.png](visualization/sales_by_customer_segment.png) |
| Relation ventes-profit | [sales_revenue_vs_profit.png](visualization/sales_revenue_vs_profit.png) |
| Matrice de corrélation | [correlation_matrix.png](visualization/correlation_matrix.png) |

## Structure du projet

```text
.
├── data/
│   └── superstore.csv
├── notebooks/
│   └── analyse_superstore.ipynb
├── visualization/
│   ├── correlation_matrix.png
│   ├── monthly_sales_revenue.png
│   ├── profit_by_region.png
│   ├── sales_by_category.png
│   ├── sales_by_customer_segment.png
│   └── sales_revenue_vs_profit.png
├── .gitignore
├── README.md
└── requirements.txt
```

Les environnements locaux tels que `.venv`, `venv` et `myenv` sont ignorés par Git.

## Installation

Exécuter les commandes suivantes depuis la racine du projet :

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Exécution

Depuis VS Code :

1. Sélectionner l'environnement virtuel créé pour le projet.
2. Ouvrir `notebooks/analyse_superstore.ipynb`.
3. Exécuter les cellules dans l'ordre.

Ou lancer Jupyter depuis PowerShell :

```powershell
jupyter notebook notebooks/analyse_superstore.ipynb
```

Le notebook détecte automatiquement la racine du projet lorsqu'il est lancé depuis la racine ou depuis le dossier `notebooks/`. Il lit `data/superstore.csv` sans modifier le fichier source et sauvegarde les graphiques dans `visualization/`.

## Technologies utilisées

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Limites

- Les résultats sont descriptifs : les corrélations observées ne démontrent pas une relation de causalité.
- Les analyses sont basées sur les données historiques disponibles et ne prédisent pas les ventes futures.
- Les remises sont étudiées par agrégation, sans tenir compte de tous les facteurs opérationnels pouvant influencer les ventes ou les profits.
