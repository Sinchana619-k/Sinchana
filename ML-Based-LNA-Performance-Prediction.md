Machine Learning-Based LNA Performance Prediction

Project Overview

This project applies machine learning techniques to predict the performance of a Low Noise Amplifier (LNA) using circuit design parameters. The objective is to learn the relationship between LNA design variables and RF performance metrics, enabling faster performance estimation and supporting data-driven circuit design.

Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- XGBoost

Methodology

1. Data Preprocessing: Load and prepare the LNA dataset for analysis.
2. Exploratory Data Analysis: Examine data distributions, potential outliers, and correlations between design parameters and performance metrics.
3. Model Development: Train Random Forest and XGBoost regression models.
4. Performance Evaluation: Evaluate model predictions using R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).
5. Model Comparison: Compare the models and select the more suitable predictor based on test-set performance.

Prediction Targets

The models predict key LNA performance metrics:

- Maximum transducer gain
- Input reflection coefficient metric (S11)
- Minimum noise figure
- Bandwidth
- Power consumption

Objective

To explore how machine learning can support LNA design by predicting RF performance from circuit parameters and reducing reliance on repeated evaluations during early-stage design exploration.

Future Work

- Integrate the trained model with multi-objective optimization using NSGA-II.
- Identify Pareto-optimal design candidates.
- Validate selected candidates through circuit simulation in Cadence Virtuoso.

Project Status

Machine learning model development, exploratory data analysis, and model evaluation have been performed. Multi-objective optimization and circuit-level validation are planned future extensions.
