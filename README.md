**Carbon Flux Prediction Using LSTM Neural Networks**

**Overview**

This project focuses on predicting carbon fluxes (e.g., Net Ecosystem Exchange, GPP, RECO) across multiple sites using long short-term memory (LSTM) neural networks. It is part of the AI4EARTH REU program at the University of Minnesota, an NSF-funded research experience for undergraduates. The project combines large-scale environmental time-series data with machine learning techniques to model and forecast ecosystem carbon dynamics.

**Features**

Predicts multiple carbon flux targets at site-level and across climate zones.

Implements advanced preprocessing for time-series environmental data.

Tracks experiments and hyperparameters using Weights & Biases (W&B).

Fully implemented in PyTorch with GPU support for accelerated training.

**Data**

Source: FluxNet environmental datasets (cleaned CSV files).

Includes site-level climate and vegetation features.

Dynamic inputs include environmental drivers such as temperature, soil water content, wind speed, radiation, and CO₂ flux measurements.

Categorical features include climate zone and plant functional types (PFT).

**Preprocessing steps:**

Missing value imputation (SimpleImputer / IterativeImputer)

Feature scaling (StandardScaler)

One-hot encoding of categorical variables

Date decomposition into day, month, and year

**Model**

Architecture: LSTM with configurable hidden layers and dropout regularization.

Inputs: Combined continuous and one-hot encoded features over sliding windows (sequence length configurable).

Outputs: Carbon flux predictions per site and target.

**Training:**

Mean Squared Error (MSE) loss

Adam optimizer with learning rate scheduling

Early stopping to prevent overfitting

**Evaluation:**

Metrics tracked include MSE, RMSE, MAE, and R²

Predictions vs. actual values plotted for analysis
