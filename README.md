Federated Learning for IoMT Intrusion Detection
Code for the manuscript: “Federated Learning for IoMT Intrusion Detection: A Communication-Efficient Topology Comparison”
This repository contains the complete implementation used in our experimental study comparing four federated learning (FL) topologies for intrusion detection in IoMT and general network environments:
•	FedAvg (Centralized Federated Averaging)
•	FCWTL (Federated Cyclic Weight Transfer Learning)
•	Ring Federated Learning
•	Gossip Federated Learning
All experiments in the manuscript were conducted under the no-attack (clean) setting.
Attack functions exist in the code for future extension but are not enabled in any of the results reported in the paper.
📁 Repository Structure
/data_preprocessing.py      # Dataset loading, cleaning, scaling, Dirichlet non-IID split
/fedavg.py                  # FedAvg implementation
/fcwtl.py                   # FCWTL implementation
/ring_fl.py                 # Ring topology implementation
/gossip_fl.py               # Gossip FL implementation
/utils.py                   # Metrics, communication cost, plotting
/main_experiments.ipynb     # Notebook to run all topologies and export results
Datasets
Experiments were performed on three benchmark datasets:
•	CICIDS2017
•	CICIoMT2024
•	WUSTL EHMS 2020
Datasets should be downloaded manually from their official sources and placed into:
/datasets/
    cicids2017/
    ciciomt2024/
    wustl/

🔧 Installation
Install all dependencies:
pip install -r requirements.txt

How to Run the Experiments
1. Preprocess datasets
python data_preprocessing.py
This generates processed non-IID client partitions for all datasets.
2. Run each topology
FedAvg
python fedavg.py
FCWTL
python fcwtl.py
Ring FL
python ring_fl.py
Gossip FL
python gossip_fl.py
Each experiment:
•	Trains 30 federated rounds
•	Evaluates accuracy, F1, precision, recall, FPR, ROC–AUC
•	Computes communication overhead
•	Saves results to /results/

 Outputs
After running all scripts, the following directory will be created:
/results/
    CICIDS2017/
    CICIOMT2024/
    WUSTL/
📌 Notes
•	All results in the paper are generated with attack_type="none".
•	Attack functions are included only for future research and are inactive by default.


