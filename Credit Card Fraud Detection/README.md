# Credit Card Fraud Detection

## Overview
This project aims to build a model for detecting credit card fraud transactions using a provided dataset. The dataset contains transactions, each labeled as either fraudulent or non-fraudulent.

## 1. Data Exploration & Preprocessing
The dataset consists of 284,807 transactions with 31 features, including:
- `Time`: Seconds elapsed between this transaction and the first transaction in the dataset.
- `V1 to V28`: Normalized features obtained through PCA transformation.
- `Amount`: Transaction amount.
- `Class`: Target variable (1 for fraudulent transactions, 0 for non-fraudulent transactions).

The dataset is highly imbalanced, with only 0.17% of transactions being fraudulent.

### Visualizations
- **Class Distribution**: Bar plot shows the imbalanced distribution of fraudulent and non-fraudulent transactions.
- **Transaction Amount & Time Distribution**: Histograms show the distribution of transaction amounts and elapsed time.
- **Correlation Matrix**: Heatmap shows the correlation between features.

## 2. Feature Engineering
- **Standardization**: The 'Amount' feature is standardized.
- **Handling Imbalanced Dataset**: Explored multiple strategies including Oversampling, Undersampling, and Adjusting Class Weights.

## 3. Model Selection & Training
- **Model**: Logistic Regression.
- **Strategies Comparison**: Trained and evaluated models using different strategies for handling class imbalance.
    1. **Baseline Model**: Without handling imbalance.
    2. **Oversampling**: SMOTE (not applicable due to library constraints).
    3. **Undersampling**: Randomly remove samples from the majority class.
    4. **Adjusting Class Weights**: Adjust the weights of the classes during model training.

### Results on Validation Set
- **Baseline Model**: High accuracy (99.92%), good balance between precision (81.67%) and recall (66.22%), F1-score (73.13%), AUC-ROC (0.83).
- **Undersampling**: High recall (87.84%), lower precision (4.49%), F1-score (8.55%), highest AUC-ROC (0.92).
- **Adjusting Class Weights**: Similar to Undersampling, high recall (86.49%), low precision (3.36%), F1-score (6.46%), AUC-ROC (0.91).

## 4. Model Evaluation
The Baseline Model is chosen for further evaluation on the test set due to its balance between precision and recall.

### Results on Test Set
- **Accuracy**: 99.93%
- **Precision** (Fraudulent Class): 92.00%
- **Recall** (Fraudulent Class): 62.16%
- **F1-score** (Fraudulent Class): 74.19%
- **AUC-ROC Score**: 0.81

### Visualizations
- **Confusion Matrix**: Shows the number of True Positives, True Negatives, False Positives, and False Negatives.
- **ROC Curve**: Plots True Positive Rate against False Positive Rate, AUC (0.81).
- **Precision-Recall Curve**: Plots Precision against Recall, Average Precision (0.74).

## Conclusion
The model demonstrates a good balance between precision and recall with high accuracy and AUC-ROC score, serving as a starting point for a credit card fraud detection system. Further tuning and optimization can be performed based on specific requirements and constraints.
