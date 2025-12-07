# TP N°4 : Apprentissage Non Supervisé - Clustering

## Objectifs

Ce TP explore deux méthodes de clustering :
- **K-Means** (centres mobiles) avec Scikit-Learn
- **CAH** (Classification Ascendante Hiérarchique) avec SciPy et Scikit-Learn
- **Divisive Clustering** (hiérarchique descendant) - implémentation custom

## Dataset

**fromage1.txt** : 29 fromages décrits par 9 attributs nutritionnels

| Attribut | Description |
|----------|-------------|
| calories | Valeur énergétique |
| sodium | Teneur en sodium |
| calcium | Teneur en calcium |
| lipides | Matières grasses |
| retinol | Vitamine A |
| folates | Vitamine B9 |
| proteines | Protéines |
| cholesterol | Cholestérol |
| magnesium | Magnésium |

## Structure du Notebook

```
tp4.ipynb
├── Compte Rendu (Markdown)
├── Partie 1 : Chargement et exploration des données
│   ├── Statistiques descriptives
│   ├── Scatter matrix
│   └── Matrice de corrélation
├── Partie 2 : K-Means
│   ├── Clustering avec k=4
│   ├── Centres des clusters
│   └── Métrique Silhouette (choix optimal de k)
├── Partie 3 : CAH
│   ├── Dendrogramme (SciPy)
│   ├── AgglomerativeClustering (Sklearn)
│   └── Comparaison CAH vs K-Means
├── Partie 4 : Interprétation
│   ├── ACP (visualisation 2D)
│   └── Divisive Clustering (implémentation)
└── Comparaisons des méthodes
```

## Méthodes de Clustering

### K-Means
- Algorithme itératif
- Nombre de clusters k fixé au départ
- Minimise l'inertie (distance intra-cluster)

### CAH (Agglomératif)
- Approche bottom-up
- Fusionne les clusters les plus proches
- Produit un dendrogramme

### Divisive (Descendant)
- Approche top-down
- Divise récursivement avec K-Means
- Implémenté manuellement dans ce TP

## Résultats Principaux

- **Meilleur k selon Silhouette** : k=2 (score: 0.507)
- **4 clusters identifiés** :
  - Cluster 0 : Fromages frais (yaourt, petit suisse)
  - Cluster 1 : Pâtes molles/persillées (camembert, roquefort)
  - Cluster 2 : Fromages de chèvre
  - Cluster 3 : Pâtes pressées cuites (emmental, comté)

## Dépendances

```bash
pip install pandas numpy matplotlib scikit-learn scipy ydata-profiling
```

## Exécution

```bash
jupyter notebook tp4.ipynb
# ou
code tp4.ipynb  # VS Code
```

## Fichiers

| Fichier | Description |
|---------|-------------|
| tp4.ipynb | Notebook principal |
| fromage1.txt | Dataset |
| fromage_report.html | Rapport YData Profiling |
| README.md | Ce fichier |
