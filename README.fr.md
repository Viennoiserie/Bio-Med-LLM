# Approche de Classification Guidée par LLM pour les Données Multi-Omics

## Tâches et Objectifs du Projet

Ce projet vise à exploiter les données multi-omiques (génomique, transcriptomique et protéomique) pour extraire des informations significatives. Notre approche comprend des tâches d'apprentissage non supervisé et supervisé :

- **Tâche Non Supervisée** : Extraire des relations significatives et identifier des clusters au sein de jeux de données complexes et de haute dimension.
- **Tâche Supervisée** : Effectuer une classification et une prédiction en utilisant l'espace d'embedding appris.

Le projet suit une méthodologie agile, utilisant GitHub pour le suivi des tâches, la surveillance des jalons et le développement collaboratif.

Pour gérer efficacement la charge de travail, le projet est divisé en trois jalons principaux avec des sous-équipes dédiées et un superviseur de projet :

1. **Prétraitement** : Recherche, sélection, nettoyage et transformation des données.
2. **Clustering** : Regroupement des données dans l'espace d'embedding à l'aide de méthodes d'apprentissage non supervisé.
3. **Classification** : Classification et prédiction à l'aide de modèles d'apprentissage supervisé.

---

## **Jalon 1 : Prétraitement**

### **1.1 Recherche et Sélection des Données**

- **Objectif** : Identifier et rassembler des ensembles de données multi-omiques appropriés, garantissant des données d'entrée diversifiées et représentatives.
- **Entrée** : Référentiels publics (par ex. TCGA, GEO, ArrayExpress, MetaboLights) contenant des données multi-omiques (génomique, transcriptomique, protéomique et métabolomique).
- **Sortie** : Un ensemble de données consolidé et annoté contenant des données multi-omiques pertinentes, y compris des séquences de protéines et d'autres données biomédicales.
- **Comment** :
  - Rechercher et examiner des ensembles de données liés à la génomique, la transcriptomique, la protéomique et la métabolomique.
  - Documenter la source, la taille, les types d'omics et les principales caractéristiques des ensembles de données.
  - Prioriser les ensembles de données ayant des échantillons qui se chevauchent sur plusieurs couches omiques.
  - S'assurer que les séquences de protéines sont adéquatement représentées pour les tâches en aval.

### **1.2 Nettoyage des Données**

- **Objectif** : Traiter les données multi-omiques manquantes, incohérentes ou erronées.
- **Entrée** : Ensembles de données bruts issus de la tâche précédente.
- **Sortie** : Ensembles de données nettoyés et annotés, prêts pour la transformation.
- **Comment** :
  - Traiter les valeurs manquantes à l'aide de techniques d'imputation spécifiques aux données biologiques, telles que l'imputation par KNN.
  - Supprimer les entrées de données en double ou non pertinentes.
  - Corriger les problèmes d'intégrité des données (par ex. alignement des séquences protéiques).
  - Normaliser les caractéristiques pour assurer la compatibilité entre les sources de données multi-omiques.

### **1.3 Transformation des Données**

- **Objectif** : Convertir les ensembles de données multi-omiques en un format adapté à l'entraînement des modèles, au clustering et à la classification.
- **Entrée** : Ensembles de données nettoyés, y compris des séquences de protéines et des données génomiques et transcriptomiques.
- **Sortie** : Ensembles de données prétraités au format structuré (par ex. matrice de caractéristiques tabulaires, embeddings pour les modèles LLM).
- **Comment** :
  - Tokeniser et embedder les séquences de protéines à l'aide de LLMs ou de modèles de bio-informatique spécialisés (par ex. ProtBERT, modèles ESM).
  - Générer des embeddings unifiés pour les données multi-omiques (par ex. concaténation ou intégration des embeddings de différentes couches omiques).
  - Effectuer la réduction de dimension si nécessaire à l'aide de méthodes comme la PCA ou l'UMAP.
  - Diviser les ensembles de données en ensembles d'entraînement, de validation et de test pour les tâches en aval.

---

## **Jalon 2 : Clustering**

### **2.1 Recherche de l'État de l'Art**

- **Objectif** : Identifier et évaluer les approches de clustering basées sur LLM pour les données multi-omiques.
- **Entrée** : Articles de recherche sur les algorithmes de clustering et les approches basées sur les transformers.
- **Sortie** : Liste documentée des méthodes de clustering basées sur LLM et justifications de la sélection.
- **Comment** :
  - Revoir la littérature sur les méthodes de clustering (par ex. k-means, clustering spectral, clustering basé sur les graphes).
  - Explorer l'utilisation des LLM pour générer des embeddings facilitant le clustering.
  - Évaluer les approches non supervisées basées sur les transformers, comme l'apprentissage contrastif ou le clustering basé sur l'attention.

### **2.2 Entraînement du Modèle**

- **Objectif** : Appliquer des modèles de clustering aux embeddings générés par les LLM.
- **Comment** :
  - Utiliser des LLMs pour générer des embeddings pour les données multi-omiques.
  - Appliquer des algorithmes de clustering sur les embeddings.
  - Ajuster les hyperparamètres pour optimiser les regroupements.

### **2.3 Évaluation du Modèle**

- **Objectif** : Évaluer la qualité du clustering et ajuster les modèles si nécessaire.
- **Comment** :
  - Évaluer la qualité du clustering à l'aide de mesures pertinentes (Silhouette Score, ARI, NMI).
  - Visualiser les résultats de clustering avec des outils de réduction de dimension (t-SNE, UMAP).

---

## **Jalon 3 : Classification**

### **3.1 Recherche de l'État de l'Art**

- **Objectif** : Identifier et évaluer les méthodes de classification basées sur LLM pour les données multi-omiques.

### **3.2 Entraînement du Modèle**

- **Objectif** : Entraîner des modèles de classification utilisant les embeddings produits par les LLMs.

### **3.3 Évaluation du Modèle**

- **Objectif** : Évaluer et comparer les modèles de classification.
- **Comment** :
  - Générer des matrices de confusion et d'autres mesures d'évaluation (précision, rappel, F1-Score, AUC-ROC).

---

## **Gestion du Projet**

- **Méthodologie Agile** : Sprints pour prioriser les tâches et suivre la progression.
- **Flux de Travail GitHub** : Suivi des jalons, tickets pour les tâches.

---

## **Responsabilités**

| **Tâche**      | **Membres de l'Équipe**  |
| -------------- | ------------------------ |
| Prétraitement  | 2 Membres                |
| Clustering     | 2 Membres                |
| Classification | 2 Membres                |
| Supervision    | 1 Membre (Chef d'équipe) |

- Après la phase de prétraitement, les membres de l'équipe sont redistribués dans d'autres groupes.

---

## **Feuille de route et jalons**

1. **Prétraitement** (semaines 1-2)

- Recherche et sélection des données
- Nettoyage des données
- Transformation des données

2. **Clustering** (semaines 3-6)

- Recherche de pointe
- Formation du modèle
- Évaluation du modèle

3. **Classification** (semaines 3-6)

- Recherche de pointe
- Formation du modèle
- Évaluation du modèle
