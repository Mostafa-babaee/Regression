**Molecular Solubility Prediction**

This project aims to predict the solubility of molecules using both traditional machine learning models and a Graph Neural Network (GNN) approach, leveraging various molecular representations.

**Project Overview**

The project involves two main approaches:

1. **Classical Machine Learning Models** using RDKit-generated descriptors.
    - **Morgan Molecular Fingerprints**: Structural fingerprint descriptors based on molecule connectivity.
    - **Molecular Properties Descriptors**: Calculated molecular properties, including molecular weight, atom count, bond count, logP, and TPSA.
2. **Graph Neural Network (GNN)** for regression, allowing for an advanced representation of molecular structure through graph-based features.

**Methodology**

**Dataset**

The dataset, based on SMILES strings and experimental log solubility values, provides essential molecular data for training and evaluation.

**Molecular Descriptors and Fingerprints**

Using RDKit, I extracted two types of descriptors:

- **Morgan Fingerprints**: Circular fingerprints with a radius of 2 and 2048-bit length.
- **Molecular Properties**: Calculated molecular weight, number of atoms, number of bonds, LogP, and TPSA.

These descriptors served as feature sets for training traditional machine learning models.

**Machine Learning Models**

The following models were trained and evaluated:

- **Ensemble Models**: AdaBoost, Extra Trees, Gradient Boosting, Random Forest.
- **Tree-Based Model**: Decision Tree.
- **Linear Model**: Ridge.
- **Other Models**: K-Neighbors, XGBoost.

**Graph Neural Network (GNN)**

To capture complex molecular structure and interaction, a GNN model was implemented using PyTorch Geometric. Each molecule was represented as a graph, where:

- **Nodes**: Represent atoms.
- **Edges**: Represent bonds. This GNN model was trained and evaluated using 5-fold cross-validation.

**Results and Evaluation**

Each model's performance was assessed using metrics such as Mean Squared Error (MSE) and R² score.

- **Classical Models** using RDKit descriptors provided valuable baseline performances.
- **GNN Model** demonstrated advanced structure-based prediction capabilities.

**Visualizations**

- **Correlation Matrix**: Analysis of descriptor correlations.
- **Distribution Plot**: Target variable distribution (log solubility).
- **Predicted vs. Actual Plot**: For each model, comparing predicted and actual solubility values.

**Usage**

1. Load dataset and generate descriptors.
2. Train models by executing the included Python scripts.
3. View model performance metrics and visualizations.

**Conclusion**

This project showcases the integration of both classical machine learning models and a GNN for molecular solubility prediction, demonstrating a comprehensive approach to molecular informatics.# Linear_regression
