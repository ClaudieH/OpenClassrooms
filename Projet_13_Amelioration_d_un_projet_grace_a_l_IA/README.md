# Amélioration assistée par IA d'une analyse de données commerciales

## Contexte

Ce projet constitue une évolution du projet Bottleneck réalisé précédemment. L'objectif n'était pas de refaire l'analyse métier, mais de démontrer une démarche professionnelle d'amélioration continue en s'appuyant sur l'intelligence artificielle générative comme outil d'assistance à la décision et au développement.

Le projet porte sur l'analyse des ventes, des stocks et de la qualité des données d'une boutique spécialisée dans la vente de vins, champagnes, cognacs et spiritueux.

---

## Objectif du projet

L'objectif principal était d'améliorer un notebook existant en appliquant une démarche critique, documentée et reproductible basée sur l'utilisation de l'IA générative.

Cette mission visait à démontrer :

- la capacité à auditer un travail existant
- l'utilisation raisonnée d'un assistant IA
- la comparaison de plusieurs solutions techniques
- la justification des choix effectués
- la traçabilité des interactions avec l'IA
- l'amélioration de la qualité des données et de la maintenabilité du projet

---

## Démarche IA

L'amélioration du projet a été menée en collaboration avec Microsoft Copilot dans une logique de co-construction et de validation systématique.

### 1. Audit du notebook initial

Premier prompt utilisé :

> "En tant que Data Scientist, analyse ce notebook et donne-moi des axes d'amélioration."

Copilot a proposé plusieurs pistes :

- amélioration de la qualité des données ;
- détection automatisée d'anomalies ;
- ajout d'interprétabilité ;
- migration vers Polars ;
- mise en place d'une démarche Data Quality.

### 2. Comparaison de solutions spécialisées

Deuxième prompt :

> "Je choisis le point Data Quality, donne-moi des modèles à améliorer dans mon notebook."

Copilot a proposé deux frameworks spécialisés :

- Pandera
- Great Expectations

### 3. Veille technologique assistée par IA

Prompt utilisé :

> "Réalise-moi une veille technologique comprenant des sources fiables pour Great Expectations."

Une veille comparative a ensuite été construite en s'appuyant sur :

- documentations officielles ;
- articles techniques spécialisés ;
- comparatifs ;
- dépôts GitHub ;
- retours d'expérience communauté.

### 4. Génération et amélioration du code

Les premières tentatives de génération directe de code n'étaient pas satisfaisantes.

Prompt initial :

> "Dans une logique d'amélioration de la qualité de la data, peux-tu détecter les anomalies avec Pandera ?"

Le résultat était incomplet et ne prenait pas en compte certaines règles métier.

Le prompt a ensuite été enrichi progressivement :

> "Dans une logique d'amélioration de la qualité de la data, peux-tu détecter les anomalies avec Pandera pour le DF ERP ?"

Puis :

> "Le contrôle des anomalies doit également prendre en compte les différences entre stock_quantity et stock_status."

Cette approche itérative a permis d'obtenir une solution répondant réellement au besoin métier.

---

## Comparaison des solutions

### Solution 1 : Great Expectations

**Forces**

- Documentation complète
- Gouvernance des données avancée
- Reporting automatique
- Adapté aux pipelines industriels

**Limites**

- Mise en place plus complexe
- Temps d'apprentissage important
- Surdimensionné pour un notebook analytique

### Solution 2 : Pandera

**Forces**

- Intégration native avec Pandas
- Déploiement rapide
- Validation déclarative
- Forte reproductibilité
- Maintenance simplifiée

**Limites**

- Nécessite la définition manuelle des règles métier
- Moins orienté gouvernance

Verdict :

> Pandera a été retenu comme meilleur compromis entre robustesse, simplicité d'implémentation, maintenabilité et reproductibilité.

---

## Améliorations apportées

### Contrôles automatisés de qualité

Mise en place de schémas de validation permettant de détecter automatiquement :

- prix négatifs
- stocks négatifs
- valeurs manquantes
- incohérences de statuts de stock
- identifiants dupliqués
- anomalies de jointure
- marges négatives
- outliers de prix

### Centralisation des règles métier

Les contrôles précédemment répartis dans de nombreuses cellules du notebook ont été regroupés dans des schémas de validation uniques afin de :

- simplifier la maintenance
- réduire les risques d'erreur
- améliorer la réutilisabilité du code

### Amélioration de la reproductibilité

Chaque exécution du notebook produit désormais les mêmes contrôles qualité et les mêmes résultats.

---

## Enseignements obtenus

Ce projet met en évidence qu'un assistant IA ne remplace pas l'expertise d'un Data Analyst.

Les expérimentations menées montrent que :

- l'IA accélère la recherche de solutions
- la qualité des résultats dépend fortement de la qualité des prompts
- plusieurs itérations sont souvent nécessaires
- les réponses doivent être systématiquement vérifiées
- l'interprétation métier reste indispensable

L'utilisation de Copilot a permis d'accélérer le développement, de structurer la réflexion technique et d'identifier des solutions pertinentes, tout en conservant une démarche critique basée sur la validation humaine.

---

## Compétences mobilisées

### Data Analysis

- Analyse exploratoire
- Contrôle qualité des données
- Analyse métier
- Validation de données

### IA Générative

- Prompt Engineering
- Évaluation critique des réponses IA
- Amélioration itérative des prompts
- Documentation des expérimentations

### Data Engineering

- Pandas
- Pandera
- Fusion de données
- Contrôles automatisés

### Gestion de projet Data

- Veille technologique
- Cahier des charges
- Gestion des risques
- Documentation technique
- Reproductibilité

---

## Résultat

Ce projet démontre une capacité à utiliser l'IA générative comme un véritable outil d'assistance professionnel en Data Analysis. L'objectif n'était pas de déléguer le travail à l'intelligence artificielle, mais de l'intégrer dans une démarche structurée de recherche, de comparaison, de validation et d'amélioration continue afin de renforcer la qualité et la fiabilité des analyses produites.
