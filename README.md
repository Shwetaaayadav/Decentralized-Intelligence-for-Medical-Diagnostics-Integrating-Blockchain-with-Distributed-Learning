# Decentralized Intelligence for Medical Diagnostics
## Federated Learning with Blockchain Verification

This project implements a decentralized healthcare diagnostic system using Federated Learning and a simulated Blockchain verification layer.

The system demonstrates how multiple hospitals can collaboratively train a heart disease prediction model without sharing raw patient data.

---

## Project Objectives

- Implement a centralized baseline model.
- Simulate multiple hospitals using federated learning.
- Apply weighted federated aggregation.
- Verify model updates using SHA256 hashing.
- Compare centralized and federated performance.
- Perform scalability analysis.

---

## Dataset

Heart Disease Dataset

- Total Samples: 1025
- Features: 13 clinical attributes
- Target: Heart Disease (0 = No Disease, 1 = Disease)

The dataset is stored inside the `data/` folder.

---

## System Architecture

### Centralized Learning
- All training data is used in one location.
- Single logistic regression model is trained.

### Federated Learning
- Training data is split into multiple simulated hospitals.
- Each hospital trains a local model.
- Only model parameters are shared.
- Global model is created using weighted averaging.

### Blockchain Verification
- Each hospital update is hashed using SHA256.
- Hashes are stored in a ledger with timestamps.
- Ensures integrity of model updates.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- SHA256 (hashlib)

---

## Performance Metrics

The following metrics are used:

- Accuracy
- Precision
- Recall
- F1 Score
- Training Time

---

## Scalability Analysis

The system evaluates performance when increasing the number of hospitals:

- 3 Hospitals
- 5 Hospitals
- 8 Hospitals

This demonstrates how decentralization affects model accuracy and computation time.

---

## Project Structure

```
Decentralized-Healthcare-Diagnostics
│
├── data/
│   └── heart.csv
│
├── notebooks/
│   └── federated_healthcare.ipynb
│
├── results/
│   ├── accuracy.png
│   ├── convergence.png
│   └── scalability.png
│
├── requirements.txt
├── README.md
└── venv/
```


### Description

- **data/** – Contains the dataset used for training and testing.
- **notebooks/** – Contains the Jupyter notebook implementing the full system.
- **results/** – Stores generated visualizations.
- **requirements.txt** – Lists all required Python packages.
- **README.md** – Documentation and instructions.
- **venv/** – Local virtual environment (excluded from version control).

---

## How to Run the Project

Follow the steps below to run the project locally.

### 1. Clone the Repository

```
git clone <repository-url>
```

### 2. Navigate to the Project Folder

```
cd Decentralized-Healthcare-Diagnostics
```

### 3. Create a Virtual Environment

```
python -m venv venv
```

### 4. Activate the Virtual Environment

Windows:
```
venv\Scripts\activate
```

Mac/Linux:
```
source venv/bin/activate
```

### 5. Install Required Dependencies

```
pip install -r requirements.txt
```

### 6. Run the Notebook

Open the notebook:

```
notebooks/federated_healthcare.ipynb
```

Run all cells sequentially from top to bottom.

---

## Key Insights

- Federated learning achieves performance comparable to centralized training.
- Raw patient data is never shared between hospitals.
- Model updates are verified using SHA256 hashing.
- Weighted aggregation ensures proportional contribution from each hospital.
- Increasing the number of hospitals introduces minor accuracy variations due to data fragmentation.

---

## Conclusion

This project demonstrates that decentralized machine learning can be effectively applied in healthcare diagnostics.

The federated learning model achieved performance similar to centralized training while preserving data privacy. The blockchain-based hashing mechanism ensured integrity of model updates without relying on a trusted central authority.

The scalability analysis highlights practical trade-offs between decentralization and performance. Overall, the implementation supports the feasibility of privacy-preserving collaborative intelligence in medical systems.
