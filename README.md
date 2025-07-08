# LLM-Guided Classification Approach for Multi-Omics Data

## Project Tasks and Objectives

This project aims to leverage multi-omics data (genomics, transcriptomics, and proteomics) to extract meaningful insights. Our approach includes both unsupervised and supervised learning tasks:

- **Unsupervised Task**: Extract meaningful relationships and identify clusters within high-dimensional, complex datasets.
- **Supervised Task**: Perform classification and prediction using the learned embedding space.

The project follows an agile methodology, utilizing GitHub for task tracking, milestone monitoring, and collaborative development.

To efficiently manage the workload, the project is divided into three core milestones with dedicated sub-teams and a project supervisor:

1. **Preprocessing**: Data research, selection, cleaning, and transformation.
2. **Clustering**: Clustering of the embedding space using unsupervised learning methods.
3. **Classification**: Classification and prediction using supervised learning models.

## **Milestone 1: Preprocessing**

### **1.1 Data Research and Selection**

- **Objective**: Identify and gather appropriate multi-omics datasets, ensuring diverse and representative input data.
- **Input**: Publicly available repositories (e.g., TCGA, GEO, ArrayExpress, MetaboLights) containing multi-omics data, including genomic, transcriptomic, proteomic, and metabolomic data.
- **Output**: A consolidated and annotated dataset containing relevant multi-omics data, such as protein sequences and other biomedical data.
- **How**:
  - Search and review datasets related to genomics, transcriptomics, proteomics, and metabolomics.
  - Document the source, size, omics types, and key characteristics of the datasets.
  - Prioritize datasets with overlapping samples across multiple omics layers.
  - Ensure protein sequences are adequately represented for downstream tasks.

### **1.2 Data Cleaning**

- **Objective**: Handle missing, inconsistent, or erroneous multi-omics data.
- **Input**: Raw datasets from the previous task.
- **Output**: Cleaned and annotated datasets ready for transformation.
- **How**:
  - Address missing values using imputation techniques specific to biological data, such as k-nearest neighbors (KNN) or domain-specific imputation methods.
  - Remove duplicate or irrelevant data entries.
  - Address data integrity issues (e.g., sequence alignment corrections for protein sequences).
  - Normalize features to ensure compatibility across multi-omics data sources.

### **1.3 Data Transformation**

- **Objective**: Convert the multi-omics datasets into a format suitable for model training, clustering, and classification.
- **Input**: Cleaned datasets, including protein sequences, genomic, and transcriptomic data.
- **Output**: Preprocessed datasets in a structured format (e.g., tabular feature matrix, embeddings for LLM models).
- **How**:
  - Tokenize and embed protein sequences using LLMs or specialized bioinformatics embedding models (e.g., ProtBERT, ESM models).
  - Generate unified embeddings for multi-omics data (e.g., concatenating or integrating embeddings from different omics layers).
  - Perform dimensionality reduction, if necessary, using methods like PCA or UMAP.
  - Split datasets into training, validation, and testing subsets for downstream tasks.

---

## **Milestone 2: Clustering**

### **2.1 State-of-the-Art Research**

- **Objective**: Identify and evaluate LLM-based clustering approaches for multi-omics data.
- **Input**: Research articles on clustering algorithms and transformer-based approaches.
- **Output**: A documented list of LLM-based clustering methods and justifications for selection.
- **How**:
  - Review literature on clustering methods for multi-omics data (e.g., k-means, spectral clustering, graph-based clustering).
  - Explore the use of LLMs to generate embeddings that facilitate clustering.
  - Evaluate transformer-based unsupervised approaches, such as contrastive learning or attention-based clustering.

### **2.2 Model Training**

- **Objective**: Apply clustering models using LLM-generated embeddings of multi-omics data.
- **Input**: Preprocessed multi-omics datasets and LLM-generated embeddings.
- **Output**: Cluster labels for each data sample.
- **How**:
  - Use LLMs (like BERT or Transformer-based models) to generate embeddings for multi-omics data.
  - Implement clustering algorithms on the embeddings (e.g., k-means, agglomerative clustering, or graph-based methods).
  - Fine-tune clustering hyperparameters to achieve optimal grouping.

### **2.3 Model Evaluation**

- **Objective**: Evaluate clustering quality and adjust models as needed.
- **Input**: Cluster labels and ground truth (if available).
- **Output**: Evaluation metrics (e.g., Silhouette Score, Adjusted Rand Index (ARI), Normalized Mutual Information (NMI)).
- **How**:
  - Measure the quality of clustering using relevant metrics.
  - Visualize clustering results using t-SNE, UMAP, or other dimensionality reduction tools.
  - Compare results across different clustering approaches and select the best method.

---

## **Milestone 3: Classification**

### **3.1 State-of-the-Art Research**

- **Objective**: Identify and evaluate LLM-based classification methods for multi-omics data.
- **Input**: Research articles on classification models and transformer-based approaches.
- **Output**: A documented list of LLM-based classification methods and justifications for selection.
- **How**:
  - Review state-of-the-art classification models for multi-omics data (e.g., decision trees, SVMs, deep learning models).
  - Explore LLM-guided classification techniques, such as transformer encoders with classification heads.
  - Consider models like BERT, ProtBERT, and multi-omics-specific transformer models.

### **3.2 Model Training**

- **Objective**: Train classification models using embeddings produced by LLMs for multi-omics data.
- **Input**: Preprocessed datasets, LLM-generated embeddings, and selected classification models.
- **Output**: Trained classification models with stored weights.
- **How**:
  - Train models on embeddings produced by LLMs.
  - Use transfer learning to leverage pre-trained models (like BERT for protein sequences) and fine-tune them for classification.
  - Employ cross-validation for robust evaluation.
  - Train classification models using Scikit-learn, TensorFlow, or PyTorch.

### **3.3 Model Evaluation**

- **Objective**: Evaluate and compare classification models for multi-omics data.
- **Input**: Model predictions and ground truth labels.
- **Output**: Evaluation metrics (e.g., Accuracy, Precision, Recall, F1-Score, ROC-AUC).
- **How**:
  - Generate confusion matrices and other evaluation metrics.
  - Use visualization tools to display the results (e.g., bar plots, ROC curves).
  - Compare performance across models to select the best-performing classification model.

---

## **Project Management**

### **Agile Methodology**

- Use **sprints** for task prioritization and progress tracking.
- Define clear milestones and objectives for each sprint.

### **GitHub Workflow**

- **Milestones**: Each milestone is detailed into subtasks.
- **Tickets**: Tasks are added as GitHub issues or pull requests.
- **Collaboration**: Team members update progress and requirements directly on GitHub.

---

## **Responsibilities**

| **Task**             | **Team Members**       |
| -------------------- | ---------------------- |
| Preprocessing        | 2 Members              |
| Clustering           | 2 Members              |
| Classification       | 2 Members              |
| Research Supervision | 1 Member (Team Leader) |

- After the preprocessing phase, team members are redistributed to other groups.

---

## **Roadmap and Milestones**

1. **Preprocessing** (Weeks 1-2)

   - Data Research and Selection
   - Data Cleaning
   - Data Transformation

2. **Clustering** (Weeks 3-6)

   - State-of-the-Art Research
   - Model Training
   - Model Evaluation

3. **Classification** (Weeks 3-6)
   - State-of-the-Art Research
   - Model Training
   - Model Evaluation
