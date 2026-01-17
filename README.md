# Dual-Layer Sybil Attack Detection for RSU-less VANETs Using Machine Learning + Proof-of-Location Framework

## Project Overview

This project presents a fully decentralized framework for detecting Sybil attacks in Vehicular Ad Hoc Networks(VANETs) operating without Road Side Units(RSUs). The system combines behavioral anomaly detection using machine learning with a physical-layer Proof-of-Location (PoL) verification mechanism to ensure that malicious vehicles forging multiple identities are accurately detected and isolated.

Realistic vehicular mobility and communication traces are generated using SUMO–Veins, enabling evaluation under dynamic and infrastructure-less traffic environments.

## Objectives

- Simulate realistic VANET communication and Sybil attack behaviors

- Extract beacon-level RSSI, timing, and mobility features

- Detect forged identities using machine learning models

- Validate suspicious nodes using cooperative Proof-of-Location
-
- Improve robustness without relying on centralized infrastructure

## Technologies & Tools Used

- **Traffic Simulator:**
  - SUMO(mobility simulation)
  - Veins(OMNeT++ + SUMO integration)
  - IEEE 802.11p/C-V2X communication

- **Programming Language:** Python

- **Machine Learning:**
  - Logistic Regression
  - Linear SVC
  - LightGBM
  - Multi-Layer Perceptron(MLP)

- **Deep Learning:** Long Short-Term Memory(LSTM)

- **Libraries & Frameworks:**
  - NumPy
  - Pandas
  - Scikit-learn
  - TensorFlow / Keras
  - Matplotlib / Seaborn

## Dataset Description

Vehicular beacon traces generated via SUMO–Veins simulations.

- **Extracted features include:**

  - RSSI variance
  - Speed deviation
  - Trajectory curvature
  - Inter-beacon timing irregularity
  - Neighbor identity stability

- **Simulated Sybil behaviors:**
  - Direct identity fabrication
  - Location spoofing
  - Colluding Sybil nodes
  - Mobility mimicking
  - Event-triggered identity bursts 

## Methodology

1. Generate mobility and communication traces using SUMO–Veins
2. Parse beacon messages and extract cross-layer features
3. Apply z-score normalization and RSSI smoothing
4. Train ML models to detect anomalous Sybil-like behavior
5. Trigger PoL verification for suspicious nodes
6. Perform RSSI-based distance estimation with multi-witness voting
7. Reject nodes failing PoL validation

## Results & Key Findings

- LightGBM AUC: 0.991

- MLP AUC: 0.982

- LSTM AUC: 0.9988

- PoL significantly reduced false positives

- Dual-layer approach improves reliability over single ML detection

## Repository Structure
```
├── data/
│   └── extracted_features.csv
├── notebooks/
│   ├── ml_models.ipynb
│   └── lstm.ipynb
├── results/
│   └── lstm_run(Results of LSTM Model)
│   └── models_compare(Results of ML Models)
├── README.md


```

 ## How to Run the Project

1. Clone the repository
```
git clone https://github.com/USERNAME/REPOSITORY_NAME.git
cd REPOSITORY_NAME
```

2. Install dependencies

```
pip install -r requirements.txt
```

3. Run the Jupyter Notebook

```
jupyter notebook
```

4. Execute:
   - ml_models.ipynb
   - lstm.ipynb

## Research Paper

Title: A Dual-Layer Sybil Attack Detection Framework for RSU-less VANETs Using Machine Learning and Proof-of-Location
This repository contains the implementation and evaluation of the proposed decentralized security framework.

## Future Enhancements

- Integrate Federated Learning for collaborative model updates

- Add trust-weighted aggregation

- Extend to large-scale VANET scenarios

- Evaluate robustness against FL model poisoning

- Adapt framework for 6G-enabled vehicular networks Improve scalability with larger and diverse road networks




