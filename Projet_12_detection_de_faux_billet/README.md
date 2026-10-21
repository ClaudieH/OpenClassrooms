# Détection automatisée de faux billets par Machine Learning

> **Compétences mobilisées :** Python • Machine Learning • Classification supervisée • Clustering • Data Cleaning • Scikit-Learn • Analyse statistique • Modélisation prédictive

## Présentation du projet

Dans le cadre d'une mission réalisée pour l'**Organisation Nationale de Lutte Contre le Faux-Monnayage (ONCFM)**, j'ai développé un système automatisé capable de déterminer si un billet est authentique ou contrefait à partir de ses caractéristiques physiques mesurées par scanner.

L'objectif consistait à comparer plusieurs algorithmes de Machine Learning recommandés par l'agence européenne EMV afin de sélectionner le modèle le plus performant et le plus exploitable en production.

---

## Problématique

**Comment automatiser la détection des faux billets en euros à partir de mesures géométriques tout en garantissant un excellent niveau de fiabilité pour les services de lutte contre la contrefaçon ?**

---

## Environnement technique

### Langage

- Python

### Bibliothèques

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

### Algorithmes étudiés

- K-Means
- Régression Logistique
- K-Nearest Neighbors (KNN)
- Random Forest

---

## Description du jeu de données

Le dataset fourni contenait :

- **1 500 billets scannés**
- **1 000 billets authentiques**
- **500 billets contrefaits**

Chaque billet est décrit par six mesures géométriques :

- Diagonal
- Height_left
- Height_right
- Margin_low
- Margin_up
- Length

---

## Analyse exploratoire

### Contrôle qualité des données

L'analyse initiale met en évidence :

- aucune valeur manquante sur cinq variables ;
- **37 valeurs manquantes sur la variable margin_low**.

### Répartition des données manquantes

Parmi les 37 valeurs manquantes :

- 29 concernent des billets authentiques ;
- 8 concernent des billets contrefaits.

---

## Nettoyage des données

### Traitement des faux billets

Les 8 faux billets comportant une valeur manquante ont été supprimés afin d'éviter toute reconstruction artificielle de données potentiellement atypiques.

### Traitement des vrais billets

L'étude statistique de la variable **margin_low** montre :

- une distribution quasi normale ;
- une faible dispersion ;
- l'absence d'outliers extrêmes ;
- de très faibles corrélations avec les autres variables.

Dans ce contexte, une imputation par la médiane (4,11 mm) a été retenue.

### Résultat du nettoyage

Le dataset final comprend :

- **1 492 billets exploitables**
- **1 000 vrais billets**
- **492 faux billets**

---

## Analyse statistique

### Validation de l'imputation

Des comparaisons ont été réalisées avant et après traitement :

- distributions
- boxplots
- heatmaps de corrélations

Les analyses montrent que l'imputation par la médiane n'a pas modifié les propriétés statistiques du jeu de données.

### Corrélations observées

La matrice de corrélation met en évidence des relations importantes entre :

- la longueur du billet
- les marges supérieures et inférieures

Ces variables apparaissent comme les plus discriminantes pour différencier les faux billets des billets authentiques.

---

# Comparaison des algorithmes

## 1. K-Means

### Objectif

Approche non supervisée visant à regrouper naturellement les billets selon leurs caractéristiques géométriques.

### Préparation

- Standardisation des variables
- Détermination du nombre optimal de clusters
- Méthode du coude
- Score de silhouette

Le nombre optimal de groupes retenu est de **2 clusters**.

### Résultats

| Indicateur | Résultat |
|------------|-----------|
| Accuracy | 98 % |
| Détection des faux billets | 97 % |


### Limites

- Modèle non supervisé
- Interprétation plus complexe
- Moins adapté à la prédiction opérationnelle

---

## 2. Régression Logistique

### Objectif

Construire un modèle explicable capable d'estimer la probabilité qu'un billet soit authentique.

### Préparation

- Découpage Train/Test
- Standardisation des variables

### Résultats

Matrice de confusion :
- 97 faux billets correctement détectés
- 199 vrais billets correctement détectés
- seulement 3 erreurs sur l'échantillon test


### Performance

| Indicateur | Résultat |
|------------|-----------|
| Accuracy | 99 % |
| AUC ROC | 0,999 |

### Variables les plus influentes

Influence positive :

- Length

Influence négative :

- Margin_low
- Margin_up
- Height_right

### Avantages

- Très rapide
- Facilement interprétable
- Justifiable auprès des autorités
- Excellentes performances

---

## 3. K-Nearest Neighbors (KNN)

### Objectif

Prédire l'authenticité en s'appuyant sur les billets les plus proches.

### Recherche du meilleur K

Après validation :

- **K optimal = 10 voisins**

### Performances

| Indicateur | Résultat |
|------------|-----------|
| Accuracy | 99 % |
| AUC | 0,989 |

### Avantages

- Très performant
- Bonne capacité à gérer des relations non linéaires

### Inconvénients

- Plus coûteux en calcul
- Nécessite la conservation des données d'apprentissage

---

## 4. Random Forest

### Objectif

Utiliser un ensemble d'arbres de décision pour améliorer la robustesse des prédictions.

### Résultats

Variables les plus importantes :

1. Length
2. Margin_low
3. Margin_up

### Performance

| Indicateur | Résultat |
|------------|-----------|
| Accuracy | 99 % |
| 1 faux négatif |
| 3 faux positifs |


### Avantages

- Très robuste
- Gestion des non-linéarités
- Importance des variables disponible

---

# Comparatif final

| Modèle | Accuracy |
|----------|----------|
| K-Means | 98 % |
| Régression Logistique | 99 % |
| KNN | 99 % |
| Random Forest | 99 % |

---

## Modèle retenu

### Régression Logistique

Le modèle sélectionné est la **Régression Logistique**.

Raisons du choix :

- Précision de 99 %
- Seulement 2 faux positifs
- Excellent score AUC
- Très faible temps d'exécution
- Forte explicabilité
- Facilité d'audit et de justification réglementaire

---

## Application de prédiction

Une application Python a été développée afin de :

1. Recevoir les dimensions d'un billet
2. Appliquer automatiquement les transformations nécessaires
3. Utiliser le modèle entraîné
4. Retourner le résultat :

- Billet authentique
- Billet contrefait

Le système est directement exploitable par les équipes de contrôle de l'ONCFM.

---

## Compétences démontrées

### Data Cleaning

- Gestion des valeurs manquantes
- Traitement d'anomalies
- Validation statistique

### Data Analysis

- Analyse exploratoire
- Corrélation
- Distribution des variables

### Machine Learning

- Clustering K-Means
- Régression Logistique
- KNN
- Random Forest

### Évaluation des modèles

- Accuracy
- AUC ROC
- Matrice de confusion
- Classification report

### Industrialisation

- Création d'un modèle prédictif
- Déploiement sous forme de script
- Aide à la décision automatisée

---

## Livrables

- Notebook d'analyse exploratoire
- Notebook de modélisation
- Script de prédiction
- Support de présentation
- Recommandation du modèle final

---

## Ce que démontre ce projet

Ce projet met en avant ma capacité à concevoir une solution complète de Machine Learning, depuis le nettoyage et la validation des données jusqu'à la comparaison rigoureuse de plusieurs algorithmes et la mise en production d'un modèle prédictif. Il démontre également ma maîtrise des problématiques de classification supervisée dans un contexte à forte exigence de fiabilité et d'explicabilité.
