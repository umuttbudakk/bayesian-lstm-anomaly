# bayesian-lstm-anomaly
# Anomaly Detection and Risk Management in Time Series

This repository contains the complete source code and experimental results for the "Bayesian LSTM Risk Radar" project, developed for the CENG463 Machine Learning Term Project.

## Project Overview
Traditional deterministic machine learning models often produce overconfident wrong predictions during financial market crashes ("Black Swans"). This project transforms a standard LSTM into a Probabilistic Bayesian Network using Monte Carlo (MC) Dropout. It acts as an early warning "Risk Radar" that dynamically expands its uncertainty bounds during out-of-distribution (OOD) events.

## Repository Structure
* `notebook.ipynb` (or `.py` files): The main code containing data preprocessing, baseline models (ARIMA, Random Forest, Standard LSTM), Optuna multi-objective tuning, and the Bayesian LSTM architecture.
* `requirements.txt`: List of dependencies required to run the project.

## How to Run
1. Clone this repository to your local machine or open the notebook directly in Google Colab.
2. Install the required dependencies:
   `pip install -r requirements.txt`
3. Run the cells in sequential order. 
   * **Note:** The hyperparameter optimization step (Optuna) takes approximately 40 minutes. You can skip the Optuna cells and directly run the "Final Architecture" section, as the optimal hyperparameters (`Window=15`, `Units=54`, `Dropout=0.097`) are already hardcoded in the final model block.

## Reproducibility
The code is fully reproducible. Running the final model block will generate the Risk Radar visualization and output the classical point-estimate metrics (MSE, RMSE, MAPE) as presented in the final LNCS report.
