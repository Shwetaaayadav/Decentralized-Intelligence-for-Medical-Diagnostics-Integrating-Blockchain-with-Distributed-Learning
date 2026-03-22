#  Decentralized Medical Diagnostics using Federated Learning

A privacy-preserving AI system that enables multiple hospitals to collaboratively train a disease prediction model **without sharing sensitive patient data**.

---

##  Key Highlights

*  Ensures **data privacy** – no raw patient data is shared
*  Simulates **multi-hospital collaboration** using federated learning
*  Achieves **performance comparable to centralized models**
*  Verifies model updates using **SHA256-based integrity checks**
*  Includes **scalability analysis** across multiple nodes

---

## Results Snapshot

* Centralized Model Accuracy: **0.7951219512195122**
* Federated Model Accuracy: **0.8048780487804879**
* Simulated Hospitals: **3, 5, 8 nodes**
* Performance gap: **Minimal (<5%) while preserving privacy**

---

##  How It Works

1. Dataset is distributed across multiple simulated hospitals
2. Each hospital trains a **local machine learning model**
3. Only model parameters are shared (not raw data)
4. Global model is created using **weighted aggregation**
5. Updates are verified using **SHA256 hashing**

---

##  System Architecture

* **Centralized Learning:** Single model trained on full dataset
* **Federated Learning:** Distributed training across multiple nodes
* **Verification Layer:** Cryptographic hashing ensures integrity

---

##  Results

### Accuracy Comparison

![Accuracy](results/Centralized vs Federated Accuracy.png)

### Model Convergence

![Convergence](results/Federated learning convergence.png)

### Scalability Analysis

![Scalability](results/Scalability Analysis.png)

---

##  Dataset

* Heart Disease Dataset
* Total Samples: **1025**
* Features: **13 clinical attributes**
* Target: **Disease prediction (0/1)**

---

##  Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* Cryptographic Hashing (SHA256)

---

##  Why This Matters

* Protects sensitive healthcare data
* Enables collaboration across institutions
* Reduces risk of data breaches
* Makes AI systems more scalable and trustworthy

---

##  How to Run

```bash
git clone <your-repo-link>
cd Decentralized-Healthcare-Diagnostics
pip install -r requirements.txt
```

Run the notebook:

```bash
notebooks/federated_healthcare.ipynb
```

---

##  Key Insights

* Federated learning achieves **near-centralized performance**
* No raw data sharing ensures **privacy compliance**
* Weighted aggregation improves fairness across nodes
* Increasing nodes introduces **minor accuracy trade-offs**

---

##  Conclusion

This project demonstrates that decentralized machine learning can be effectively applied in healthcare systems. By combining federated learning with cryptographic verification, the system achieves strong performance while maintaining data privacy and trust.

---
