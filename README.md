# Classification Temporelle de Textes avec Embeddings Contextuels

Ce projet vise à classifier des textes en fonction de leur période de publication (entre 1820 et 2023) en utilisant des modèles de langage pré-entraînés adaptés au français. Les modèles étudiés sont **CamemBERT**, **Flaubert**, et **mBERT**. Ce travail évalue leurs performances et identifie des pistes d'amélioration pour des tâches similaires.

---

## Introduction
Les tâches de classification temporelle sur des textes longs posent des défis, notamment :
- La gestion de l'évolution linguistique sur des périodes étendues.
- Les limites des méthodes non contextuelles, qui échouent à saisir les nuances sémantiques complexes.

L'objectif principal est de comparer les performances de plusieurs modèles basés sur les transformers (CamemBERT, Flaubert, mBERT) pour classifier des textes en intervalles temporels de 20 ou 40 ans.

---

## Pipeline de Classification

### Étapes Principales
1. **Prétraitement des Données :**
   - Nettoyage et tokenisation des textes.
   - Transformation des textes en embeddings contextuels.
2. **Classification :**
   - Entraînement des modèles avec des labels correspondant aux périodes temporelles.
3. **Évaluation :**
   - Analyse des performances à l'aide des métriques : Précision, Rappel, F1-score, et Exactitude.

### Données Utilisées
- **Corpus :** 1 051 textes, fournis par des experts.
- **Périodes Temporelles :**
  - **20 ans :** 1820–1839, 1840–1859, ..., 2000–2023.
  - **40 ans :** 1820–1859, 1860–1899, ..., 1980–2023.

---

## Modèles Utilisés

### CamemBERT
- Modèle de type BERT, pré-entraîné spécifiquement pour la langue française.
- Performant pour les tâches monolingues en français.

### Flaubert
- Une alternative à CamemBERT, avec des optimisations supplémentaires pour le français.

### mBERT
- Modèle multilingue conçu pour traiter plus de 100 langues.
- Moins performant pour des tâches spécifiques à une langue, comme le français.

---

## Résultats Principaux

### Résumé des Performances
| Modèle      | Intervalle | Précision Moyenne | Rappel Moyen | F1-Score Moyen | Exactitude |
|-------------|------------|-------------------|--------------|----------------|------------|
| CamemBERT   | 20 ans     | 0.39              | 0.36         | 0.36           | 0.36       |
| CamemBERT   | 40 ans     | 0.61              | 0.60         | 0.57           | 0.59       |
| Flaubert    | 20 ans     | 0.45              | 0.42         | 0.39           | 0.42       |
| Flaubert    | 40 ans     | 0.53              | 0.52         | 0.50           | 0.51       |
| mBERT       | 20 ans     | 0.35              | 0.28         | 0.25           | 0.28       |
| mBERT       | 40 ans     | 0.32              | 0.39         | 0.27           | 0.30       |

### Analyse
- CamemBERT et Flaubert surpassent mBERT pour les deux intervalles.
- Les intervalles de 40 ans permettent de meilleurs résultats grâce à des données mieux équilibrées.

---

## Points Forts et Limites

### Points Forts
- **Modèles spécialisés pour le français :** CamemBERT et Flaubert offrent des performances supérieures grâce à leur pré-entraînement sur des données françaises.
- **Pipeline robuste :** Prétraitement et entraînement optimisés pour des résultats fiables.

### Limites
- **Déséquilibre des données :** Les classes correspondant à certaines périodes sont sous-représentées.
- **Performance des intervalles courts :** Les intervalles de 20 ans montrent des performances plus faibles.

---

## Améliorations Futures
1. **Augmentation de Données :**
   - Sur-échantillonnage des classes sous-représentées.
   - Utilisation de techniques comme SMOTE ou substitution par synonymes.
2. **Ensembles de Modèles :**
   - Tester des pipelines combinant les forces de plusieurs modèles pour améliorer les performances.
3. **Exploration Linguistique :**
   - Étudier davantage les effets de l’évolution linguistique dans les données historiques.

---

## Comment Lancer le Projet

### Prérequis
- Python 3.7+
- Jupyter Notebook

### Étapes
1. Clonez ce dépôt :
   ```bash
   git clone <URL_du_dépôt>
