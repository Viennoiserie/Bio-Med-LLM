# State-of-the-Art in Multi-Omics Data Integration and Classification

## Articles

Below are key articles that support our approach. Each article includes a summary, the proposed approach, and details on datasets and authors.

### 1. **CLCLSA: Cross-omics Linked Embedding with Contrastive Learning and Self-Attention for Multi-Omics Integration with Incomplete Data**

- **Resume**: This paper proposes CLCLSA, a method that addresses incomplete multi-omics data integration. It introduces cross-omics autoencoders to represent features from multiple omics layers. Using contrastive learning and self-attention, the model maximizes the mutual information between omics types, significantly enhancing integration and clustering performance.
- **Approach**:
  - **Embedding**: Cross-omics autoencoder to project data into a unified latent space.
  - **Learning**: Uses contrastive learning to align cross-omics representations and applies a self-attention mechanism to focus on key features.
  - **Problem Solved**: Efficiently handles incomplete multi-omics data and improves integration and clustering performance.
- **Dataset**: The authors tested the method on public datasets like TCGA (The Cancer Genome Atlas) and other synthetic datasets with missing data patterns.
- **Authors**: Lin Wang, Wei Xu, and colleagues from the Department of Bioinformatics, arXiv.

---

### 2. **Comparative Analysis of Multi-Omics Integration Using Advanced Graph Neural Networks for Cancer Classification**

- **Resume**: This study explores the use of Graph Neural Networks (GNNs) for cancer classification from multi-omics data. GNNs are well-suited to handling the non-linear and high-dimensional nature of multi-omics data. The paper provides a comparative analysis of different GNN architectures and demonstrates their superior performance in cancer classification tasks.
- **Approach**:
  - **Embedding**: Graph-based embedding to capture relationships among omics data.
  - **Learning**: Uses GNNs to model complex inter-relationships between nodes (representing omics features) and learns meaningful representations for cancer classification.
  - **Problem Solved**: Enhances cancer classification accuracy by capturing non-linear relationships within multi-omics datasets.
- **Dataset**: Public datasets like TCGA, METABRIC (breast cancer), and GEO datasets.
- **Authors**: Zongxiang Liu, Fan Zhang, and colleagues from the School of Artificial Intelligence, arXiv.

---

### 3. **SDGCCA: Supervised Deep Generalized Canonical Correlation Analysis for Multi-Omics Integration**

- **Resume**: This paper introduces a deep learning-based approach for multi-omics integration called SDGCCA. The method aligns shared features from multiple omics datasets while preserving unique features specific to each omics layer. It also facilitates the discovery of biomarkers.
- **Approach**:
  - **Embedding**: Deep generalized canonical correlation analysis to link shared features across multiple omics layers.
  - **Learning**: Supervised learning is used to optimize feature alignment and facilitate classification.
  - **Problem Solved**: It effectively aligns shared features and identifies important biomarkers from multi-omics data.
- **Dataset**: Data from AMP-AD (Alzheimer’s Disease Knowledge Portal) and publicly available multi-omics datasets.
- **Authors**: Yifan Zhang, Lin Fan, and collaborators from Shanghai Jiao Tong University, arXiv.

---

### 4. **DEDUCE: Multi-head Attention Decoupled Contrastive Learning to Discover Cancer Subtypes Based on Multi-Omics Data**

- **Resume**: DEDUCE introduces a new method for discovering cancer subtypes. It employs multi-head attention to identify shared and distinct features across omics datasets. Decoupled contrastive learning is then applied to separate common features from subtype-specific ones, which improves clustering and classification.
- **Approach**:
  - **Embedding**: Multi-head attention to identify shared and distinct feature patterns.
  - **Learning**: Decoupled contrastive learning is used to better differentiate between common and unique features.
  - **Problem Solved**: This approach allows for the discovery of cancer subtypes using shared and distinct patterns.
- **Dataset**: Cancer-related multi-omics datasets from TCGA and other cancer-related public datasets.
- **Authors**: Liangrui Pan, Xiaoyu Zhang, and colleagues from Huazhong University of Science and Technology, arXiv.

---
