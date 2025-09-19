# NeurIPS - Open Polymer Prediction 2025

Machine learning models for predicting polymer properties from SMILES molecular representations, intended for the [NeurIPS competition](https://www.kaggle.com/competitions/neurips-open-polymer-prediction-2025).

## Approach

The goal of the competition was to predict the following properties: Glass transition temperature (Tg), Free fractional volume (FFV), Thermal conductivity (Tc), Density, Radius of gyration (Rg). This projects explores both a more traditional approach and the use of neural networks.

1. **Gradient Boosting** (`01_gradient_boosting.ipynb`) - AutoGluon ensemble with RDKit descriptors, Morgan fingerprints, and MACCS keys
2. **Enhanced Features** (`02_feature_engineering.ipynb`) - Target-specific feature combinations including 3D conformational descriptors and transformer embeddings
3. **Graph Neural Networks** (`03_graph_nn.ipynb`) - Multi-task GNN learning directly from molecular graphs
4. **Model Ensemble** (`04_ensemble.ipynb`) - Weighted combination optimised for each target property

## Data

- Primary training data: `data/train.csv`
- Supplementary datasets: `data/train_supplement/`
- No external data was used

## Usage

Run notebooks sequentially to reproduce the competition pipeline. Models are saved to `models/` for ensemble combination and final predictions.