# NeurIPS - Open Polymer Prediction 2025
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


Machine learning models for predicting polymer properties from SMILES molecular representations, intended for the [NeurIPS Polymer Prediction competition](https://www.kaggle.com/competitions/neurips-open-polymer-prediction-2025).

## Approach

The goal of the competition was to predict the following properties: Glass transition temperature (Tg), Free fractional volume (FFV), Thermal conductivity (Tc), Density, Radius of gyration (Rg). This projects explores both a more traditional approach and the use of neural networks.

1. `01_gradient_boosting.ipynb` - AutoGluon ensemble with RDKit descriptors, Morgan fingerprints, and MACCS keys
2. `02_feature_engineering.ipynb` - Target-specific feature combinations including 3D conformational descriptors and transformer embeddings
3. `03_graph_nn.ipynb` - Multi-task GNN learning directly from molecular graphs
4. `04_ensemble.ipynb` - Weighted combination optimised for each target property

## Usage

Run notebooks sequentially to reproduce the competition pipeline. Models are saved to `models/` for ensemble combination and final predictions.
