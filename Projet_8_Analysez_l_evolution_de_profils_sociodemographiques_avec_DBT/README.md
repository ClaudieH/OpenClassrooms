# Analyse de l'évolution des profils sociodémographiques avec DBT

> **Compétences mobilisées :** DBT • Snowflake • SQL • Data Engineering • Data Quality • Data Governance • RGPD • Analyse de données

## Présentation du projet

Dans le cadre d'une mission réalisée pour OpenClassrooms, j'ai conçu un pipeline de transformation de données avec DBT afin d'analyser l'évolution du profil sociodémographique des apprenants des parcours Data sur plusieurs années.

L'objectif était de produire des données fiables, documentées et réutilisables afin d'aider les équipes pédagogiques et stratégiques à mieux comprendre les profils des apprenants et à évaluer l'accessibilité des formations. 

### Documentation DBT

La documentation technique générée automatiquement avec DBT Docs est disponible ici :

🔗 ** [Consulter la documentation DBT](https://claudieh.github.io/dbt-docs/#!/overview)**

Cette documentation présente :

- Le lineage des modèles
- Les sources de données
- Les transformations réalisées
- Les dépendances entre modèles
- Les tests de qualité des données
- Les descriptions des tables et colonnes

---

## Problématique

**Comment construire un pipeline analytique fiable permettant d'étudier l'évolution des profils des apprenants tout en garantissant qualité des données, traçabilité et conformité RGPD ?**

---

## Environnement technique

### Data Engineering

- DBT (Data Build Tool)
- Snowflake

### Analyse de données

- SQL

### Sources

- Données internes OpenClassrooms
- Données publiques INSEE

---

## Travaux réalisés

### Préparation des données

- Contrôle de la qualité des données
- Gestion des valeurs manquantes
- Harmonisation des formats
- Standardisation des données géographiques et démographiques
- Contrôle des identifiants et des doublons

### Construction du pipeline DBT

- Création des modèles de transformation
- Structuration des couches Staging, Intermediate et Marts
- Documentation complète des traitements
- Mise en place de tests de qualité automatisés
- Génération de la documentation DBT

### Enrichissement des données

- Intégration de données démographiques INSEE
- Croisement avec les données OpenClassrooms
- Construction d'indicateurs sociodémographiques exploitables

### Analyse des profils

Étude de l'évolution :

- Du nombre d'apprenants
- De la répartition hommes/femmes
- De la répartition géographique
- Des tendances observées sur plusieurs années

---

## Principaux résultats

### Évolution des effectifs

L'analyse met en évidence une baisse du nombre d'inscriptions après 2022 suivie d'un regain d'activité à partir de 2024 pour les parcours Data d'OpenClassrooms.

### Différences de représentation selon le parcours

La comparaison entre les formations OpenClassrooms et les parcours académiques traditionnels montre une représentation féminine plus importante dans les cursus classiques, alors que les parcours OpenClassrooms restent majoritairement masculins sur la période étudiée.

### Répartition géographique stable

La distribution géographique des apprenants reste relativement stable au fil du temps et suit globalement les grands bassins de population.

### Accessibilité des formations

L'étude met en évidence l'importance de la formation à distance pour faciliter l'accès aux parcours Data sur l'ensemble du territoire, notamment dans les régions éloignées des principaux pôles universitaires.

---

## Valeur apportée

Cette mission a permis :

- De fiabiliser les données utilisées pour les analyses
- De documenter l'ensemble des transformations
- De rendre les analyses reproductibles
- De comparer les profils OpenClassrooms avec des données nationales
- De fournir aux équipes métier des indicateurs fiables pour le pilotage stratégique

---

## Compétences démontrées

### Data Engineering

- Développement de pipelines DBT
- Documentation automatisée
- Industrialisation des transformations

### Data Quality

- Contrôle qualité des données
- Tests automatisés
- Validation des règles métier

### SQL & Snowflake

- Requêtes analytiques
- Jointures complexes
- Création d'indicateurs

### Gouvernance des données

- Documentation
- Traçabilité
- Conformité RGPD

### Analyse de données

- Analyse sociodémographique
- Analyse comparative
- Interprétation de tendances

---

## Livrables

- Projet DBT documenté
- Documentation DBT Docs
- Modèles SQL
- Dictionnaire des données
- Présentation des résultats
- Recommandations métier

---

## Ce que démontre ce projet

Ce projet illustre ma capacité à concevoir un pipeline de transformation de données moderne avec DBT, à mettre en œuvre des bonnes pratiques de qualité et de gouvernance des données, puis à produire des analyses fiables permettant de transformer des données brutes en informations exploitables pour la prise de décision.
