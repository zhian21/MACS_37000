# MACS_37000 - Social Network Analysis and Link Prediction

This repository contains datasets, preprocessed data, models, and scripts used for analyzing social networks and predicting link formation using homophily and structural similarity. The primary datasets include **Eurobarometer (EU), Facebook SNAP, and Pokec**, which have been preprocessed to ensure consistency across experiments.

---

## 📂 Repository Structure

```
MACS_37000
│── 📂 dataset/                 # Preprocessed datasets (Eurobarometer, Facebook, Pokec)
│   ├── 📂 EU/                   # Eurobarometer dataset
│   │   ├── eu_preprocessed.ipynb   # Preprocessing script
│   │   ├── eu.csv                  # Cleaned dataset
│   │   ├── gender_norm.sav          # Survey data (raw)
│   │   ├── Codebook.pdf             # Metadata and documentation
│   ├── 📂 facebook/              # Facebook social network data (SNAP dataset)
│   │   ├── facebook_preprocessed.ipynb  # Preprocessing script
│   │   ├── facebook_preprocessed.csv    # Cleaned dataset
│   │   ├── facebook_combined.txt        # Raw text data (preprocessed)
│   ├── 📂 pokec/                 # Pokec social network dataset
│       ├── final_pokec_dataset.csv   # Cleaned dataset
│       ├── pokec_preprocessed.ipynb  # Preprocessing script
│       ├── soc-pokec-profiles.txt.gz  # Raw compressed profiles
│       ├── soc-pokec-relationships.txt.gz # Raw compressed relationships
│
│── 📂 model/                   # Model outputs and embeddings
│   ├── model_1.csv             # Model 1 results
│   ├── model_2_edges.csv       # Edges for Model 2 (Homophily + Structure)
│   ├── model_2_nodes.csv       # Nodes for Model 2
│   ├── model_2_node_embeddings.txt  # Node2Vec embeddings (Model 2)
│   ├── model_3_edges.csv       # Edges for Model 3 (Homophily-Only)
│   ├── model_3_nodes.csv       # Nodes for Model 3
│   ├── pokecu_valid.ipynb      # Validation script for Pokec dataset
│
│── 📂 literature review/       # Research articles and references
│
│── README.md                   # Documentation for repository
```

---

## 📖 Project Overview

This project explores **link prediction in social networks** using demographic similarity (homophily) and structural properties. We construct synthetic networks, train **GraphSAGE** models for link prediction, and validate them on the **Pokec** social network.

### 🔑 Key Components
- **Preprocessed Datasets**: Standardized versions of **Eurobarometer, Facebook SNAP, and Pokec**, ensuring alignment in sociodemographic attributes.
- **Synthetic Network Generation**: Models incorporating **homophily and structural similarity** to simulate realistic social connections.
- **Graph Embeddings**: **Node2Vec** applied to extract feature representations.
- **Link Prediction Models**: **GraphSAGE** trained on synthetic networks and tested on **Pokec**.

---

## 🚀 Usage

### **1. Clone the Repository**
```bash
git clone https://github.com/zhian21/MACS_37000.git
cd MACS_37000
```

### **2. Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3. Run Preprocessing Scripts**
#### 📌 **Eurobarometer**
```bash
cd dataset/EU
jupyter notebook eu_preprocessed.ipynb
```
#### 📌 **Facebook**
```bash
cd dataset/facebook
jupyter notebook facebook_preprocessed.ipynb
```
#### 📌 **Pokec**
```bash
cd dataset/pokec
jupyter notebook pokec_preprocessed.ipynb
```

### **4. Train Models**
```bash
cd model/
jupyter notebook model2.ipynb   # Homophily + Structure
jupyter notebook model1.ipynb   # Baseline Model
```

### **5. Validate on Pokec**
```bash
cd model/
jupyter notebook pokecu_valid.ipynb
```

---

## 📊 Results

- **Synthetic networks** successfully replicate real-world homophily patterns.
- **GraphSAGE models** exhibit strong predictive performance on synthetic data but struggle on **Pokec** due to latent, unmodeled factors.
- **Structural similarity improves link prediction**, but generalizability remains limited.

---

## 📜 Citations

- **Facebook SNAP Dataset**: Leskovec, J. & McAuley, J. (2012). Learning to discover social circles in ego networks.
- **Pokec Dataset**: Takac, L. & Zabovsky, M. (2012). Data analysis in public social networks.
- **Eurobarometer Survey**: European Commission. (2022). Eurobarometer Data.

