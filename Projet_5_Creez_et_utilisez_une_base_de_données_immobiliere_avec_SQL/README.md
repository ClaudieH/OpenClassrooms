# Conception et exploitation d'une base de données immobilière décisionnelle 

> **Compétences mobilisées :** SQL • Modélisation de données • Data Architecture • Gouvernance des données • Data Quality • Analyse immobilière • Data Management • Business Analysis

## Présentation du projet

Dans le cadre d’une mission de conseil réalisée pour **Laplace Immo**, réseau national d’agences immobilières, j’ai été chargé de concevoir une base de données relationnelle permettant de centraliser, structurer et exploiter des données immobilières issues de sources publiques.

L’objectif était de construire un socle de données fiable permettant aux équipes métier de mieux comprendre les dynamiques du marché immobilier et de préparer le développement futur de modèles prédictifs d’aide à la décision.

---

## Contexte et enjeu métier

Le marché immobilier génère de grands volumes de données provenant de nombreuses sources externes :

- Transactions immobilières
- Données démographiques
- Données territoriales
- Référentiels géographiques

Ces données sont souvent hétérogènes et difficilement exploitables en l’état.

Laplace Immo souhaite mettre en place une architecture de données cohérente afin de :

- Centraliser l’information
- Garantir la qualité et la cohérence des données
- Faciliter les analyses immobilières
- Produire des indicateurs de marché fiables
- Préparer le développement futur de modèles de valorisation immobilière.

---

## Problématique

**Comment concevoir une base de données relationnelle robuste permettant de transformer plusieurs sources de données immobilières en un outil d'aide à la décision exploitable par les agences du réseau ?**

---

## Sources de données

La base a été construite à partir de plusieurs jeux de données open data :

### Données immobilières

- DVF (Demandes de Valeurs Foncières)
- Transactions immobilières
- Caractéristiques des biens

### Données démographiques

- Données communales de l'INSEE
- Population des communes

### Données territoriales

- Référentiel géographique national
- Régions
- Départements
- Communes

Ces différentes sources ont été consolidées dans un modèle de données unique.

---

## Environnement technique

### Base de données

- SQL

### Modélisation

- SQL Power Architect
- Modèle Conceptuel de Données (MCD)
- Schéma relationnel
- Normalisation 3NF

### Documentation

- Dictionnaire des données
- Documentation fonctionnelle
- Présentation métier

---

## Démarche de conseil

### 1. Analyse du besoin métier

Identification des besoins des équipes immobilières :

- Suivi de l'évolution des prix
- Analyse géographique des transactions
- Étude des volumes de ventes
- Comparaison des marchés régionaux
- Préparation de futurs modèles de prévision

### 2. Gouvernance et compréhension des données

Construction d'un dictionnaire permettant de documenter :

- Les attributs métiers
- Les règles de gestion
- Les règles de calcul
- Les contraintes de qualité des données

### 3. Modélisation de la base

Conception d'un modèle relationnel en identifiant :

- Les entités
- Les relations
- Les cardinalités
- Les clés primaires
- Les clés étrangères

Le modèle a ensuite été normalisé jusqu'à la troisième forme normale (3NF) afin de garantir la cohérence et de limiter la redondance des données.

### 4. Mise en conformité

Vérification :

- De l'intégrité référentielle
- De la cohérence des données
- Du respect des principes RGPD
- Des règles de gouvernance des données

### 5. Exploitation analytique

Développement de requêtes SQL destinées à répondre à des problématiques métier concrètes :

- Analyse des ventes
- Évolution des prix
- Comparaisons régionales
- Analyse des transactions
- Classements immobiliers

---

## Architecture de données réalisée

Le modèle final repose sur plusieurs entités principales :

### Région

Informations administratives régionales.

### Commune

Informations géographiques et démographiques.

### Bien

Caractéristiques détaillées des biens immobiliers :

- Type de bien
- Surface
- Nombre de pièces

### Vente

Historique des transactions immobilières :

- Date de vente
- Valeur foncière
- Bien concerné

Cette structure garantit la cohérence et la maintenabilité de la base.

---

## Analyses réalisées

La base de données a permis de répondre à plusieurs problématiques métier :

### Analyse de l'activité immobilière

- Nombre total de ventes
- Répartition des ventes par région
- Évolution des transactions dans le temps

### Analyse des prix

- Prix moyen au mètre carré
- Classement des départements les plus chers
- Comparaison entre types de biens
- Analyse des écarts de prix selon le nombre de pièces

### Analyse territoriale

- Classement des régions
- Communes les plus dynamiques
- Transactions rapportées à la population
- Comparaisons géographiques.

---

## Principaux enseignements

### Forte concentration du marché en Île-de-France

Les analyses mettent en évidence un volume de transactions particulièrement important en Île-de-France ainsi qu'un prix moyen au mètre carré significativement supérieur à la moyenne nationale.

### Disparités territoriales importantes

Les écarts observés entre régions et départements démontrent l'importance d'une analyse localisée du marché immobilier.

### Corrélation entre caractéristiques et valeur du bien

La surface, le type de bien et le nombre de pièces apparaissent comme des variables structurantes pour l'analyse du marché et la future modélisation prédictive. 

---

## Valeur apportée au métier

Ce projet a permis de doter l'entreprise :

- D'une base de données centralisée et exploitable
- D'un référentiel de données documenté
- D'une architecture fiable et évolutive
- D'un socle analytique permettant la production d'indicateurs immobiliers
- D'une fondation technique pour de futurs projets de data science et de valorisation immobilière
