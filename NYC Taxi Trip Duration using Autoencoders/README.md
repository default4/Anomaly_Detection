## Overview

This project focuses on detecting anomalies in the New York City Taxi Trip Duration dataset using Autoencoders. Anomalies in this context refer to taxi trips with unusual durations that could be the result of various factors such as traffic, driver behavior, or technical issues. The primary goal of this project is to identify these anomalies, which can help in further analysis and optimization of taxi services.

## Dependencies

* Python 3.x
* NumPy
* pandas
* scikit-learn
* seaborn
* matplotlib
* TensorFlow 2.x

To install the dependencies, run the following command:

```
pip install numpy pandas scikit-learn seaborn matplotlib tensorflow
```

## Dataset

The dataset used in this project is the New York City Taxi Trip Duration dataset, available on Kaggle. You can download the dataset here (https://www.kaggle.com/c/nyc-taxi-trip-duration/data).

The dataset contains information about taxi trips in New York City, such as pickup and dropoff locations, pickup datetime, and trip duration. The main objective of the project is to detect anomalies in the trip duration. The dataset is preprocessed and scaled before being used for training and evaluation.