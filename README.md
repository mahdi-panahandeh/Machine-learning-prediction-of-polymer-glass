# Machine Learning Prediction of Polymer Glass Transition Temperature


## Overview
Prediction of polymer glass transition temperature (Tg) 
from SMILES representations using multiple ML approaches 
including XGBoost, Graph Neural Networks, and ChemBERTa.

## Key Results
| Model | Test R² | MAE |
|-------|---------|-----|
| Linear Regression | 0.755 | 37.5°C |
| Random Forest | 0.871 | 27.9°C |
| XGBoost | 0.879 | 25.8°C |
| GNN (GAT + edge features) | 0.855 | 28.8°C |
| ChemBERTa | 0.866 | 27.6°C |

## Key Findings
- RingCount is the dominant predictor of Tg (53% importance)
- High-confidence predictions achieve MAE=14.5°C
- ML screening can reduce experimental workload by ~40%

## Dataset
7,284 polymers with experimental Tg values
- Source: PolyInfo database
- Features: 205 RDKit molecular descriptors

## Methods
- Molecular descriptors from SMILES using RDKit
- XGBoost with hyperparameter tuning
- Graph Neural Network with attention mechanism
- Transfer learning with ChemBERTa
- Uncertainty quantification via Random Forest variance

## Installation
pip install -r requirements.txt

## Usage
jupyter notebook notebooks/03_xgboost_model.ipynb

## Author
Mahdi Panahandeh
Department of Polymer Chemistry
University of Tehran
