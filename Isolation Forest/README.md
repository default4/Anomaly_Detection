## Overview

This project demonstrates how to implement anomaly detection using the Isolation Forest algorithm in Python. We use the credit card fraud dataset available on Kaggle for this purpose. The dataset contains anonymized credit card transactions, with a small proportion of them being fraudulent. The goal is to detect these fraudulent transactions using the Isolation Forest algorithm.

## Dependencies

* Python 3.7+
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

To install the dependencies, run the following command:

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Dataset

The dataset used in this project is the credit card fraud dataset available on Kaggle. You can download the dataset here (https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). The dataset contains anonymized credit card transactions, with a small proportion of them being fraudulent. There are a total of 31 columns in the dataset, including 'Time', 'Amount', and 28 anonymized features (V1, V2, ..., V28). The 'Class' column is the target variable, with '1' indicating a fraudulent transaction and '0' indicating a non-fraudulent transaction.

After downloading the dataset, place the creditcard.csv file in the same directory as the project script.