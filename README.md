# Player Engagement Prediction Using Machine Learning

This project investigates the use of machine learning models to predict player engagement levels based on behavioral gameplay data.

In this project, engagement prediction is formulated as a multi-class classification problem (Low, Medium, High), allowing for interpretable player segmentation.

The goal is to build and compare different machine learning models while identifying key behavioral factors that influence engagement.

## Models
The following models are implemented and evaluated:

- Logistic Regression 
- Support Vector Machine (RBF kernel)
- Random Forest
- XGBoost

## Methodology

### Data Processing
- Categorical variables encoded (one-hot / label encoding)
- Feature scaling applied where necessary (SVM, Logistic Regression)
- No missing data handling required
- Stratified sampling used to preserve class distribution

### Training & Evaluation
- 80/20 train-test split
- Stratified cross-validation for model stability
- Evaluation metrics:
  - Accuracy
  - Macro F1-score
  - Confusion matrix

### Optimization
- Hyperparameter tuning using RandomizedSearchCV
- Early stopping and regularization for XGBoost
- Model-specific optimization strategies applied

## Results

- Logistic Regression: ~87% accuracy
- SVM: ~90% accuracy
- Random Forest: ~92% accuracy
- XGBoost: ~92.5% accuracy

Ensemble models achieved the best performance, demonstrating the importance of capturing non-linear relationships in behavioral data.

## Key Insights

- Engagement is primarily driven by **behavioral intensity**, not demographic features
- Most important features:
  - Session frequency
  - Average session duration
  - Total playtime
- Misclassifications mostly occur between adjacent engagement levels (ordinal structure)

## Dataset

The dataset contains ~40,000 player records including:
- Gameplay statistics 
- Demographic information
- Engagement labels (Low, Medium, High)

## How to Run

- Jupyter Notebook
- Google Colab

Required libraries:
- pandas
- scikit-learn
- xgboost

