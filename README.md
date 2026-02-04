# SafeSlope V1 – Dual-Model AI Framework for Landslide Risk Assessment

SafeSlope Version-1 is a research-based AI system designed to assess landslide risk by separating
temporal rainfall triggers from spatial vulnerability patterns.

The project adopts a dual-model architecture:
- LSTM for rainfall trend prediction (WHEN risk increases)
- DNN for landslide vulnerability classification (WHERE risk exists)

This repository represents the baseline implementation prior to hybrid model integration.

---
## Contributors

SafeSlope is a collaborative research-based project developed with clearly defined responsibilities.

- Harshit Bhatt – Lead Developer  
  Designed and implemented all machine learning models, including LSTM for rainfall trend prediction and DNN for landslide risk classification. Responsible for model architecture, coding, training, evaluation, and system integration.

- Anjali Sharma – Research & Documentation Lead  
  Conducted literature review, research analysis, model justification, performance interpretation, and complete project documentation. Contributed to problem formulation, result analysis, and research presentation.

- Saumy Singh – Data Engineering & Preprocessing  
  Handled data collection, extraction, cleaning, preprocessing, feature preparation, and dataset structuring for both rainfall and landslide datasets.

Each contributor played a critical role in building SafeSlope Version-1.


## Problem Statement
Landslides are complex natural disasters influenced by both dynamic environmental factors
(rainfall patterns) and static geographical vulnerability (terrain, soil, and historical events).
Most traditional systems fail to model these factors independently.

SafeSlope addresses this gap using specialized deep learning models.

---

## Model Architecture

### 1. Rainfall Prediction Model (LSTM)
- Input: Daily rainfall time-series data
- Features: Rolling rainfall (7-day, 30-day)
- Output: Rainfall trend and hazard level
- Purpose: Detect rainfall buildup and trigger conditions

### 2. Landslide Risk Classification Model (DNN)
- Input: Historical landslide incident reports
- Technique: TF-IDF text vectorization
- Output: Risk class (LOW / MEDIUM / HIGH)
- Purpose: Identify geographically vulnerable districts

---

## Performance Summary

### LSTM Model
- R² Score: 0.97
- Trend Accuracy: 95%
- Extremely low MAE and RMSE

### DNN Model
- Macro AUC: 0.92
- High precision and recall for vulnerable zones
- Limited HIGH-risk samples due to dataset imbalance

---

## Key Insight
Landslide risk cannot be predicted using rainfall or location alone.

SafeSlope demonstrates that:
> Risk = Rainfall Trigger × Geographical Vulnerability

---

## Current Status
✔ Individual models validated  
✔ Performance benchmarks achieved  
⏳ Hybrid model integration (Version-2 in progress)

---

## Future Work (Version-2)
- Combine LSTM and DNN outputs into a unified risk score
- Integrate terrain slope, soil type, and land-use features
- Develop early-warning risk visualization system

---

## Disclaimer
This project is intended for academic and research purposes and does not replace
official disaster warning systems.
