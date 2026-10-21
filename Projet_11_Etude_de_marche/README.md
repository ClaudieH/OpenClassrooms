# Étude de marché internationale pour l'exportation de poulets biologiques

> **Compétences mobilisées :** Python • Data Analysis • ACP (PCA) • Clustering • Machine Learning • Analyse PESTEL • Open Data • Data Visualisation • Business Analysis

## Présentation du projet

Dans le cadre d'une mission réalisée pour l'entreprise **La Poule Qui Chante**, spécialisée dans la production de poulets issus de l'agriculture biologique, j'ai conduit une étude exploratoire visant à identifier les marchés internationaux les plus pertinents pour soutenir une stratégie de développement à l'export.

L'objectif était de sélectionner des pays présentant un potentiel commercial élevé à partir de données économiques, démographiques, logistiques et alimentaires, puis de les regrouper en segments homogènes grâce à des méthodes statistiques avancées.

---

## Problématique

**Quels sont les pays offrant les meilleures opportunités pour développer l'exportation de poulets biologiques à l'international ?**

---

## Environnement technique

### Analyse de données

- Python
- Pandas
- NumPy

### Data Visualisation

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-Learn
- ACP (Analyse en Composantes Principales)
- Classification Ascendante Hiérarchique (CAH)
- K-Means

### Sources de données

- FAO (Food and Agriculture Organization)
- Banque mondiale
- Données démographiques internationales

---

## Démarche

### Analyse PESTEL

Afin d'identifier les variables pertinentes pour l'étude, une analyse PESTEL a été réalisée.

Les indicateurs retenus couvrent plusieurs dimensions :

| Dimension | Variables retenues |
|------------|-------------------|
| Sociale | Population, croissance démographique |
| Économique | PIB par habitant, inflation, évolution de l'inflation |
| Économique | Importations de volaille |
| Économique | Disponibilité intérieure |
| Économique | Dépendance alimentaire |
| Technologique | Indice logistique |
| Politique | Stabilité politique |

---

## Préparation des données

### Collecte et enrichissement

Consolidation de plusieurs sources :

- Données FAO relatives à la filière volaille
- Données démographiques mondiales
- Données logistiques de la Banque mondiale
- Données économiques et politiques internationales

### Nettoyage et harmonisation

Les travaux réalisés comprennent :

- Filtrage sur la viande de volaille
- Harmonisation des noms de pays
- Traduction des nomenclatures internationales
- Gestion des valeurs manquantes
- Création de variables dérivées
- Fusion de plusieurs bases de données

### Feature Engineering

Création notamment de :

- La dépendance alimentaire
- La croissance démographique
- La croissance de l'inflation


### Couverture des données

La base finale comporte :

- **165 pays analysés ;**
- **96,4 % de la population mondiale couverte.**

---

## Analyse exploratoire

### Étude des distributions

Analyse des principales variables :

- Importations de volaille
- Disponibilité intérieure
- Dépendance alimentaire
- Population
- Inflation
- PIB par habitant
- Stabilité politique

Cette étape a permis d'identifier les dispersions importantes et les pays atypiques à prendre en compte avant la phase de modélisation.

---

## Réduction de dimension avec l'ACP

Les variables ont été standardisées afin de les placer sur une même échelle avant l'analyse.

### Résultats

L'ACP montre que :
- 5 composantes principales permettent d'expliquer plus de **80 % de la variance totale**
- Ces composantes résument efficacement les informations du jeu de données.

### Principaux axes identifiés

#### PC1 : Développement économique et institutionnel

Axe décrivant :

- Le niveau de richesse
- La qualité logistique
- La stabilité politique

#### PC2 : Pression démographique et alimentaire

Axe représentant :

- La taille de la population
- La disponibilité alimentaire
- La pression sur la consommation

#### PC3 : Volatilité économique

Axe porté principalement par :

- L'inflation
- L'évolution de l'inflation

#### PC4 : Vulnérabilité alimentaire

Axe lié à :

- La dépendance alimentaire
- La croissance démographique

#### PC5 : Comportements atypiques

Axe permettant d'identifier les situations particulières.

---

## Clustering des pays

### Classification Ascendante Hiérarchique (CAH)

Une première segmentation a été réalisée à partir des composantes principales.

Le score de silhouette identifie un découpage optimal en **2 groupes**.

### K-Means

Une seconde segmentation a ensuite été effectuée à l'aide de K-Means.

Après analyse :

- Méthode du coude
- Score de silhouette

le nombre optimal retenu est de **3 clusters**.

---

## Principaux résultats

### Cluster prioritaire

Le cluster le plus attractif regroupe des pays caractérisés par :

- Un fort niveau de développement économique
- Une bonne stabilité politique
- Une logistique performante
- Une demande importante
- Une pression démographique favorable


### Construction d'un score de recommandation

Un score multicritère a été développé en intégrant :

- Les importations
- La dépendance alimentaire
- La démographie
- Le PIB
- La logistique
- L'inflation
- La stabilité politique

### Top pays identifiés

Les premiers pays obtenus sont :

1. Hong Kong
2. Japon
3. Allemagne
4. Belgique
5. Royaume-Uni

---

## Recommandation finale

Après prise en compte des contraintes géographiques et commerciales, les pays retenus sont :

### Allemagne

- Marché développé
- Excellente logistique
- Forte proximité géographique
- Facilité des échanges au sein de l'Union européenne

### Belgique

- Marché mature
- Forte accessibilité
- Proximité culturelle et géographique
- Position stratégique pour la distribution européenne

---

## Compétences démontrées

### Data Preparation

- Fusion de sources multiples
- Qualité des données
- Feature engineering

### Analyse exploratoire

- Analyse PESTEL
- Analyse multivariée
- Détection d'anomalies

### Statistiques avancées

- ACP
- Cercle des corrélations
- Projection d'individus

### Machine Learning

- Classification Ascendante Hiérarchique
- K-Means
- Évaluation par silhouette

### Business Analysis

- Étude de marché internationale
- Scoring multicritère
- Aide à la décision stratégique

---

## Livrables

- Notebook de préparation des données
- Notebook ACP et clustering
- Présentation de restitution
- Recommandations stratégiques
- Analyse comparative des marchés

---

## Ce que démontre ce projet

Ce projet illustre ma capacité à conduire une étude de marché internationale fondée sur les données, depuis la collecte et la préparation de sources hétérogènes jusqu'à la mise en œuvre de méthodes statistiques avancées. Il démontre également ma maîtrise de l'ACP, du clustering et de l'analyse multicritère pour transformer des données complexes en recommandations stratégiques exploitables par les décideurs.
