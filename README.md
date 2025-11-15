
# Federated Learning for IoMT Intrusion Detection  
**Code repository for the manuscript:**  
**“Federated Learning for IoMT Intrusion Detection: A Communication-Efficient Topology Comparison”**

This repository contains the full implementation used to generate all experimental results reported in the manuscript. The study evaluates four communication-efficient Federated Learning (FL) topologies for network intrusion detection in Internet of Medical Things (IoMT) environments:

- **FedAvg** – Centralized Federated Averaging  
- **FCWTL** – Federated Cyclic Weight Transfer Learning  
- **Ring Federated Learning**  
- **Gossip Federated Learning**

All experiments in the paper were conducted under the **clean (no-attack)** setting.  
Attack-related functions exist in the development version of the project but were **not used** to generate any results in the manuscript.

---

## 📁 Repository Contents

README.md → Project overview and instructions
requirements.txt → Python dependencies
main-experiments.ipynb → Complete FL pipeline (preprocessing + training + evaluation)
results-baseline.zip → Baseline evaluation results (metrics, plots, curves)

The notebook includes:
- Dataset preprocessing  
- Non-IID Dirichlet client partitioning  
- Implementation of all four FL topologies  
- Metrics computation (Accuracy, F1, Precision, Recall, FPR, ROC–AUC)  
- Communication overhead estimation  
- Plot generation and result export  

---

## 📊 Datasets Used

Experiments were performed on three publicly available intrusion detection datasets:

- **CICIDS2017**  
- **CICIoMT2024**  
- **WUSTL EHMS 2020**

Due to licensing and size limitations, datasets are **not included** in this repository.  
They must be downloaded from their official sources and loaded into the notebook.

---

## 🔧 Installation

Use Python **3.8+** and install dependencies:

```bash
pip install -r requirements.txt
________________________________________
▶️ Running the Experiments
Open:
main-experiments.ipynb
Execute the notebook sequentially to:
1.	Preprocess datasets
2.	Generate non-IID client splits
3.	Train all four FL topologies (30 rounds each)
4.	Evaluate performance (Accuracy, Precision, Recall, F1-score, FPR, ROC–AUC)
5.	Compute communication overhead per topology
6.	Export and visualize results
All results are automatically generated during execution.
________________________________________
📂 Provided Results
Baseline results used in the manuscript are included as:
results-baseline.zip
This archive contains:
•	Accuracy/Loss curves
•	Confusion matrices
•	Evaluation metrics (CSV)
•	Communication overhead summaries
These correspond strictly to the no-attack setting used in the study.
________________________________________
📌 Notes
•	All results in the paper were obtained with attack_type="none".
•	Attack functions are included only for future research and remain inactive in all reported experiments.
•	This repository ensures full reproducibility of the experimental workflow presented in the manuscript.
________________________________________
