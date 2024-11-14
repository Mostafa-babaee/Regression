**Molecular Solubility Prediction**

This project predicts the solubility of molecules using traditional machine learning models and a Graph Neural Network (GNN) approach, leveraging various molecular representations for enhanced accuracy.

**Project Overview**

This project involves two main approaches:

1. **Classical Machine Learning Models** using RDKit-generated descriptors:
    - **Morgan Molecular Fingerprints**: Structural descriptors based on molecule connectivity.
    - **Molecular Properties Descriptors**: Calculated properties, including molecular weight, atom count, bond count, logP, and TPSA.
2. **Graph Neural Network (GNN)** for regression, offering an advanced graph-based representation of molecular structure.

**Methodology**

**Dataset**

The dataset consists of SMILES strings and experimental log solubility values, providing essential molecular data for training and evaluation.

**Molecular Descriptors and Fingerprints**

Using RDKit, I extracted two types of descriptors:

- **Morgan Fingerprints**: Circular fingerprints with radius 2 and 2048-bit length.
- **Molecular Properties**: Calculated properties like molecular weight, atom and bond counts, LogP, and TPSA.

These descriptors served as feature sets for traditional machine learning models.

**Machine Learning Models**

The following models were trained and evaluated:

- **Ensemble Models**: AdaBoost, Extra Trees, Gradient Boosting, Random Forest
- **Tree-Based Model**: Decision Tree
- **Linear Model**: Ridge
- **Other Models**: K-Neighbors, XGBoost

**Graph Neural Network (GNN)**

To capture complex molecular structures and interactions, I implemented a GNN model using PyTorch Geometric, representing each molecule as a graph where:

- **Nodes** represent atoms.
- **Edges** represent bonds.

The GNN model was trained and evaluated using 5-fold cross-validation.

**Results and Evaluation**

Each model’s performance was assessed using Mean Squared Error (MSE) and R² score.

- **Classical Models** with RDKit descriptors provided valuable baseline performances.
- **GNN Model** demonstrated advanced structure-based prediction capabilities.

**Results:**

1. **Using RDKit Morgan Molecular Fingerprints as Descriptors**:
    - **AdaBoost**: MSE = 2.6, R² = 0.408
    - **Decision Tree**: MSE = 2.255, R² = 0.487
    - **Extra Trees**: MSE = 2.086, R² = 0.525
    - **Gradient Boosting**: MSE = 1.713, R² = 0.610
    - **K-Neighbors**: MSE = 2.279, R² = 0.481
    - **Random Forest**: MSE = 1.418, R² = 0.677
    - **Ridge**: MSE = 1.501, R² = 0.658
    - **XGBoost**: MSE = 1.319, R² = 0.700
2. **Using RDKit Molecular Properties as Descriptors**:
    - **AdaBoost**: MSE = 0.838, R² = 0.809
    - **Decision Tree**: MSE = 0.936, R² = 0.787
    - **Extra Trees**: MSE = 0.579, R² = 0.868
    - **Gradient Boosting**: MSE = 0.605, R² = 0.862
    - **K-Neighbors**: MSE = 1.520, R² = 0.654
    - **Random Forest**: MSE = 0.565, R² = 0.871
    - **Ridge**: MSE = 0.995, R² = 0.774
    - **XGBoost**: MSE = 0.648, R² = 0.852
3. **Graph Neural Network (GNN) Regression Model**:
    - **Average MSE (5 folds)**: 3.148
    - **Average R² (5 folds)**: 0.278

**Visualizations**

- **Correlation Matrix**: Analysis of descriptor correlations.
- **Distribution Plot**: Distribution of target variable (log solubility).
- **Predicted vs. Actual Plot**: Comparing predicted and actual solubility values for each model.

**Usage**

1. Load the dataset and generate descriptors.
2. Train models by executing the included Python scripts.
3. View model performance metrics and visualizations.

**Conclusion**

This project showcases a comprehensive approach to molecular solubility prediction, combining classical machine learning models and a GNN to leverage different molecular representations for improved predictive accuracy.
