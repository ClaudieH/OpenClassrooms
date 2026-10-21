# 🌍 Projet 4 - Réalisez une étude de santé publique avec Python
 
> **Compétences mobilisées :** Python • Pandas • Data Wrangling • Data Analysis • Data Visualisation • Analyse Statistique • Santé Publique • Business Intelligence • Storytelling

## Présentation du projet

Dans le cadre d’une mission d’analyse de données pour une organisation internationale, j’ai réalisé une étude de la sécurité alimentaire mondiale à partir des données de la FAO (Food and Agriculture Organization).

L’objectif était d’évaluer la disponibilité alimentaire mondiale, mesurer l’ampleur de la sous-nutrition et identifier les pays les plus vulnérables afin de produire des indicateurs permettant d’éclairer les politiques publiques et les actions humanitaires.

---

## Contexte et enjeu métier

La lutte contre la faim constitue l’un des principaux objectifs de développement durable définis par les Nations Unies.

Malgré une production alimentaire mondiale historiquement élevée, plusieurs centaines de millions de personnes restent touchées par la sous-nutrition.

Cette étude vise à répondre aux questions suivantes :

- Les ressources alimentaires mondiales permettent-elles théoriquement de nourrir l’ensemble de la population ?
- Comment les ressources alimentaires sont-elles réparties ?
- Quels usages sont faits de la production agricole mondiale ?
- Quels pays sont les plus touchés par la sous-nutrition ?
- Quels enseignements peuvent orienter les politiques de sécurité alimentaire ?

---

## Problématique

**Comment expliquer la persistance de la sous-nutrition dans le monde alors que la production alimentaire mondiale semble suffisante pour couvrir les besoins de la population ?**

---

## Sources des données

Les données proviennent de la FAO et couvrent principalement la période 2013-2017.

Jeux de données utilisés :

- Population mondiale par pays
- Disponibilité alimentaire
- Sous-nutrition
- Aide alimentaire internationale

Les données ont été consolidées afin d'obtenir une vision globale des ressources alimentaires disponibles et de leur répartition.

---

## Environnement technique

### Langage

- Python

### Bibliothèques

- Pandas
- NumPy
- Matplotlib
- Seaborn

### Méthodes

- Data Cleaning
- Jointures de données
- Analyse exploratoire (EDA)
- Agrégation de données
- Construction d'indicateurs
- Analyse statistique descriptive
- Data Visualisation

---

## Démarche analytique

### 1. Préparation et fiabilisation des données

Les données provenant de plusieurs sources ont nécessité :

- La vérification de leur qualité ;
- Le traitement des valeurs manquantes ;
- L'harmonisation des unités de mesure ;
- La standardisation des formats ;
- La consolidation de plusieurs jeux de données.

### 2. Analyse de la sous-nutrition

Construction d'indicateurs permettant de mesurer :

- Le nombre de personnes sous-alimentées ;
- Le taux de sous-nutrition par pays ;
- L'évolution de la sous-nutrition dans le temps ;
- Les zones géographiques les plus exposées.

### 3. Analyse de la disponibilité alimentaire

Étude de :

- La disponibilité alimentaire mondiale
- La disponibilité alimentaire par habitant
- La capacité théorique du système alimentaire mondial à nourrir la population

### 4. Analyse des flux alimentaires

Analyse de l'utilisation des ressources agricoles entre :

- L'alimentation humaine
- L'alimentation animale
- Les pertes alimentaires
- Les usages industriels
- Les semences

### 5. Analyse géopolitique

Identification :

- Des pays les plus touchés par la sous-nutrition
- Des principaux bénéficiaires de l'aide alimentaire internationale
- Des disparités régionales en matière de sécurité alimentaire

---

## Principaux résultats

### Une production mondiale théoriquement suffisante

L'analyse montre qu'en 2017 les ressources alimentaires mondiales disponibles permettaient théoriquement de nourrir environ **10,6 milliards de personnes**, soit largement plus que la population mondiale estimée à **7,5 milliards d'habitants**.

### Persistance de la sous-nutrition

Malgré cette disponibilité théorique, près de **535 millions de personnes** souffraient de sous-nutrition, représentant environ **7,1 % de la population mondiale**.

### Importance de l'alimentation animale

L'étude met en évidence qu'une part importante des céréales mondiales est destinée à l'alimentation animale (**36,3 %**), contre **42,7 %** destinée directement à l'alimentation humaine.

### Impact des pertes alimentaires

Près de **4,6 %** de la disponibilité alimentaire mondiale est perdue avant consommation, représentant un levier important d'amélioration de la sécurité alimentaire.

### Pays les plus touchés par la sous-nutrition

Les pays présentant les proportions les plus élevées de personnes sous-alimentées comprennent notamment :

- Haïti (48 %)
- Corée du Nord (47 %)
- Madagascar (41 %)
- Lesotho (38 %)
- Tchad (38 %)

### Cas d'étude : la Thaïlande

L'analyse du manioc en Thaïlande illustre les paradoxes des systèmes alimentaires mondiaux :

- 9 % de la population demeure sous-alimentée
- plus de 83 % de la production de manioc est exportée
- la disponibilité alimentaire moyenne reste pourtant suffisante pour couvrir les besoins nutritionnels

---

## Valeur apportée à la décision

Cette étude permet de démontrer que les problématiques de sous-nutrition sont moins liées à une insuffisance de production qu'à des enjeux de :

- Répartition des ressources
- Utilisation des productions agricoles
- Organisation des échanges internationaux
- Accès économique à l'alimentation

L'analyse fournit ainsi des indicateurs pouvant soutenir les décisions des organismes publics, ONG et institutions internationales.

---

## Recommandations

### Réduire les pertes alimentaires

Mettre en œuvre des politiques visant à limiter les pertes tout au long de la chaîne d'approvisionnement afin d'améliorer l'efficacité alimentaire mondiale.

### Optimiser l'utilisation des céréales

Réévaluer l'allocation des ressources destinées à l'alimentation animale lorsque des situations critiques de sécurité alimentaire sont observées.

### Prioriser les zones à risque

Concentrer les programmes d'aide alimentaire sur les pays présentant à la fois :

- Un taux élevé de sous-nutrition
- Une faible disponibilité alimentaire par habitant
- Une dépendance importante aux importations alimentaires

### Développer les outils d'aide à la décision

Mettre en place des tableaux de bord permettant un suivi régulier des indicateurs de sécurité alimentaire à l'échelle internationale.

---

## Limites de l'étude

- Données agrégées à l'échelle nationale
- Absence de données infra-nationales permettant une analyse régionale fine
- Approche descriptive sans modélisation prédictive
- Données limitées à la période étudiée

---

## Perspectives

- Développer un modèle prédictif du risque d'insécurité alimentaire
- Construire une cartographie interactive mondiale de la sous-nutrition
- Intégrer des variables climatiques et économiques
- Étudier l'impact des conflits géopolitiques sur la disponibilité alimentaire
- Réaliser une segmentation des pays selon leur niveau de vulnérabilité alimentaire

---

## Compétences démontrées

### Data Engineering & Data Preparation

- Nettoyage et transformation de données
- Harmonisation de sources multiples
- Jointures complexes
- Contrôle qualité

### Data Analysis

- Analyse exploratoire
- Construction d'indicateurs
- Analyse statistique descriptive
- Analyse comparative internationale

### Data Visualisation

- Création de visualisations décisionnelles
- Synthèse graphique des résultats
- Communication de données complexes

### Business & Public Policy Analysis

- Compréhension des enjeux de sécurité alimentaire
- Analyse d'indicateurs de santé publique
- Identification de leviers d'action
- Recommandations stratégiques

---

## Livrables

- Notebook Python
- Rapport d'analyse
- Support de présentation
- Visualisations et indicateurs de synthèse

---

## Ce que démontre ce projet

Ce projet illustre ma capacité à exploiter des données complexes issues de sources multiples afin de répondre à une problématique de santé publique à grande échelle. Il met en évidence ma capacité à transformer des données brutes en indicateurs décisionnels, à identifier des leviers d'amélioration et à communiquer des résultats à destination de décideurs non techniques.
 
J'ai appris à manipuler plusieurs sources de données, construire des analyses fiables et produire des visualisations permettant de transformer des données complexes en informations compréhensibles et exploitables pour la prise de décision.
