# Classification Temporelle de Textes avec Embeddings Contextuels

## Introduction
Ce projet explore la classification temporelle de textes en utilisant des modèles de langage pré-entraînés pour le français, tels que **CamemBERT**, **Flaubert**, et **mBERT**. L'objectif principal est d'évaluer leurs performances dans la distinction temporelle des textes publiés entre 1820 et 2023.

## Pipeline de Classification
1. **Prétraitement des données :**
   - Tokenisation des textes.
   - Extraction des embeddings contextuels.
2. **Classification :**
   - Entraînement des modèles sur des intervalles temporels définis (20 ans et 40 ans).
   - Prédiction et évaluation des résultats.
3. **Évaluation :**
   - Précision moyenne, rappel moyen, F1-score moyen, et exactitude.

## Modèles Utilisés
- **CamemBERT** : Spécialisé pour le français, basé sur BERT.
- **Flaubert** : Optimisé pour le français, similaire à BERT.
- **mBERT** : Multilingue, capable de traiter plus de 100 langues.

## Résultats Principaux
| Modèle      | Intervalle | Précision Moyenne | Rappel Moyen | F1-Score Moyen | Exactitude |
|-------------|------------|-------------------|--------------|----------------|------------|
| CamemBERT   | 20 ans     | 0.39              | 0.36         | 0.36           | 0.36       |
| CamemBERT   | 40 ans     | 0.61              | 0.60         | 0.57           | 0.59       |
| Flaubert    | 20 ans     | 0.45              | 0.42         | 0.39           | 0.42       |
| Flaubert    | 40 ans     | 0.53              | 0.52         | 0.50           | 0.51       |
| mBERT       | 20 ans     | 0.35              | 0.28         | 0.25           | 0.28       |
| mBERT       | 40 ans     | 0.32              | 0.39         | 0.27           | 0.30       |

## Points Forts et Limites
- **Points Forts :**
  - CamemBERT et Flaubert surpassent mBERT pour le français.
  - Bonne performance pour les intervalles de 40 ans.
- **Limites :**
  - Déséquilibre des données dans les intervalles de 20 ans.
  - mBERT moins performant pour le traitement en français.

## Améliorations Futures
1. Augmenter le corpus en sur-échantillonnant les classes sous-représentées et en utilisant des techniques comme SMOTE.
2. Combiner plusieurs modèles pour un pipeline d'ensemble.
3. Étudier l'impact de l'évolution linguistique en approfondissant le traitement temporel.

## Comment Lancer le Projet
1. Clonez ce dépôt :  
   ```bash
   git clone <URL_du_dépôt>
