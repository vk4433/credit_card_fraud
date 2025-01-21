
## Setup Instructions

### 1. Create Conda Environment
To create a new Conda environment with Python 3.12, run the following command:
```bash
conda create -p env python==3.12
```

### 2. Install Dependencies
After creating the environment, activate it and install the required dependencies using pip:
```bash
pip install -r requirements.txt
```

## Project: Credit Card Fraud Detection
This project aims to detect fraudulent credit card transactions using machine learning algorithms. The dataset used for this project contains transactions made by credit cards in September 2013 by European cardholders. The dataset includes transactions that occurred over two days, with 492 frauds out of 284,807 transactions. This information is sourced from Kaggle.

## Data Preprocessing
The dataset contains no null values, and all columns are numerical. We removed duplicate entries and saved the preprocessed data to a CSV file. Additionally, oversampling and undersampling techniques were applied due to the dataset's significant imbalance.

## Dataset
The dataset can be downloaded from Kaggle. It includes the following features:
- **Time**: Number of seconds elapsed between this transaction and the first transaction in the dataset.
- **V1 to V28**: Results of a PCA transformation.
- **Amount**: Transaction amount.
- **Class**: 1 for fraudulent transactions, 0 otherwise.

## Supervised Machine Learning
In this project, supervised machine learning techniques are used to build a model that predicts fraudulent transactions. The following steps were taken:

### Data Preprocessing
The dataset contains no null values, and all columns are numerical. Duplicate entries were removed, and the preprocessed data was saved to a CSV file. Oversampling and undersampling techniques were applied due to the dataset's imbalance.

### Feature Selection
Relevant features contributing to the prediction of fraudulent transactions were selected. All features were found to be moderately correlated.

### Model Training
Various supervised machine learning models, including Logistic Regression and XGBoost, were trained.

### Model Evaluation
The performance of the trained models was evaluated using metrics such as accuracy, precision, recall, and F1-score.

### Model Selection
The best-performing model was selected based on the evaluation metrics.

### Results Using XGBoost
- **Accuracy**: 0.9763
- **Precision**: 0.9878
- **Recall**: 0.9647
- **F1 Score**: 0.9761

The goal was to achieve a high precision rate to effectively identify fraudulent transactions.

## NOte
i had tried  hyperparameters by using Gridsearch my system is not compactble i had waited more then 150+ min

## Unsupervised Machine Learning
In addition to supervised learning, unsupervised machine learning techniques were explored. The following steps were taken:

### Outlier Detection
During outlier removal, 62% of the data was lost. Therefore, the Isolation Forest model was chosen for unsupervised learning as it handles large datasets effectively, even with outliers.

### Oversampling Techniques
Oversampling was performed to improve accuracy by comparing the original true values and the predicted values.

### Results Using Isolation Forest
- **Accuracy**: 0.5449
- **Precision**: 0.9537
- **Recall**: 0.0944
- **F1 Score**: 0.1718

## Conclusion
This project utilized both supervised and unsupervised machine learning techniques to build models capable of detecting fraudulent credit card transactions.

- **Supervised Learning**: XGBoost achieved high precision and recall, making it effective for fraud detection.
- **Unsupervised Learning**: Isolation Forest was employed to handle outliers, but it demonstrated lower performance compared to supervised methods.

The project highlights the importance of balancing precision and recall in fraud detection tasks.
