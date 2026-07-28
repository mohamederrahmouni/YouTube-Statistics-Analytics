# YouTube Statistics Analytics

Analyse exploratoire des statistiques des chaînes YouTube les plus populaires au monde : abonnés, vues, revenus estimés, pays d'origine, type de contenu, et facteurs socio-économiques associés (population, taux de chômage, éducation...).

Le projet couvre l'ensemble du pipeline d'analyse de données : nettoyage, analyse univariée, bivariée, multivariée, analyse temporelle/spatiale, ainsi qu'un tableau de bord Power BI pour la restitution visuelle.

## Contenu du dépôt

```
├── data/
│   ├── Global-YouTube-Statistics.csv               # Dataset brut
│   ├── Global-YouTube-Statistics_cleaned.csv        # Dataset nettoyé
│   └── Global-YouTube-Statistics_duplicates_dropped.csv
├── notebooks/
│   ├── AnalyseUnivariée.ipynb                       # Exploration variable par variable
│   ├── AnalyseBivariée.ipynb                        # Relations entre deux variables
│   ├── AnalyseMultivariée.ipynb                     # Relations multi-variables (PCA, etc.)
│   └── Analyse_Temporelle_ Spatiale _Spatio-temporelle.ipynb
└── Dashboard-PowerBI/
    └── Youtube-Stat-Analytics.pbix.zip              # Tableau de bord interactif
```

## Dataset

Le jeu de données regroupe, pour chaque chaîne YouTube, des informations telles que : le nombre d'abonnés, le nombre de vues, le pays d'origine, la catégorie/type de chaîne, les revenus estimés (mensuels et annuels), la date de création de la chaîne, ainsi que des indicateurs socio-économiques du pays (population, taux de chômage, taux de scolarisation dans le supérieur, population urbaine, coordonnées géographiques...).

## Analyses réalisées

- **Analyse univariée** : distribution des abonnés, des vues, des revenus, répartition par pays et par catégorie.
- **Analyse bivariée** : relations entre variables qualitatives et quantitatives (ex. pays vs vues), corrélations entre indicateurs.
- **Analyse multivariée** : visualisations combinées (barplots groupés, réduction de dimension avec PCA) pour croiser plusieurs variables à la fois.
- **Analyse temporelle, spatiale et spatio-temporelle** : évolution du nombre de chaînes/vues dans le temps, répartition géographique des chaînes et de leur performance.
- **Dashboard Power BI** : synthèse visuelle et interactive des principaux indicateurs.

## Technologies utilisées

- **Python** (Jupyter Notebook)
- **Pandas**, **NumPy** : manipulation des données
- **Matplotlib**, **Seaborn** : visualisation
- **Scikit-learn** (PCA, StandardScaler, MinMaxScaler) : réduction de dimension et normalisation
- **Statsmodels**, **SciPy** : lissage (LOWESS), détection de pics, statistiques
- **GeoPandas**, **Geopy**, **Shapely**, **Geodatasets** : analyse et visualisation géospatiale
- **Power BI** : dashboard interactif

## Installation et utilisation

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/mohamederrahmouni/YouTube-Statistics-Analytics.git
   cd YouTube-Statistics-Analytics
   ```

2. Installer les dépendances :
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy geopandas geopy shapely geodatasets
   ```

3. Ouvrir les notebooks dans Jupyter :
   ```bash
   jupyter notebook notebooks/
   ```

4. Pour le dashboard, ouvrir le fichier `.pbix` (après extraction du zip) avec **Power BI Desktop**.


