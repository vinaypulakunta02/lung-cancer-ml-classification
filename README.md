# Lung Cancer Classification Using Machine Learning

## Overview

This project demonstrates a Machine Learning workflow for classifying clinical observations into **cancer** and **non-cancer** groups using a lung cancer clinical dataset.

The project is implemented in Python using Google Colab and includes data preprocessing, feature selection, model training, prediction, and evaluation.

## Objective

The objective of this project is to apply a supervised Machine Learning approach to clinical data and classify observations into cancer and non-cancer groups based on available clinical and lifestyle-related features.

## Dataset

The dataset used in this project is the **Lung Cancer Dataset** available on Kaggle.

**Dataset Source:**

https://www.kaggle.com/datasets/akashnath29/lung-cancer-dataset

The dataset contains clinical and lifestyle-related variables including:

- Gender
- Age
- Smoking
- Yellow Fingers
- Anxiety
- Peer Pressure
- Chronic Disease
- Fatigue
- Allergy
- Wheezing
- Alcohol Consuming
- Coughing
- Shortness of Breath
- Swallowing Difficulty
- Chest Pain

### Target Variable

The target variable is:

`LUNG_CANCER`

The target classes are:

- `YES` = Cancer
- `NO` = Non-cancer

The original dataset is not included in this repository. The dataset should be obtained from the original Kaggle source and used according to its applicable license and attribution requirements.

---

## Machine Learning Workflow

The project follows the following workflow:

```text
Clinical Dataset
       ↓
Data Loading
       ↓
Data Preprocessing
       ↓
Feature and Target Separation
       ↓
Train-Test Split
       ↓
Feature Selection
       ↓
Random Forest Model Training
       ↓
Prediction
       ↓
Model Evaluation

1. Data Loading

The clinical dataset is uploaded and loaded into a Pandas DataFrame using Python.

The dataset structure and initial observations are examined before performing preprocessing.

2. Data Preprocessing

Data preprocessing is performed to prepare the clinical dataset for Machine Learning.

Duplicate records are removed from the dataset.

The categorical GENDER variable is converted into numerical form:

M → 1
F → 0

The target variable LUNG_CANCER is also converted into numerical form:

YES → 1
NO → 0

Missing values are checked before continuing with the Machine Learning workflow.

3. Feature and Target Separation

The clinical variables are separated from the target variable.

The clinical variables are used as input features, while LUNG_CANCER is used as the target variable.

The Machine Learning model learns the relationship between the clinical features and the cancer classification.

4. Train-Test Split

The dataset is divided into training and testing sets.

80% of the data is used for training.
20% of the data is used for testing.

The training dataset is used to train the Machine Learning model, while the testing dataset is kept separate for evaluating the model on previously unseen observations.

Stratified splitting is used to maintain the proportion of the target classes in both training and testing datasets.

5. Feature Selection

Feature selection is performed using the Mutual Information method.

Mutual Information measures the amount of information provided by a feature about the target variable.

The 10 most informative features are selected for the Machine Learning model.

Feature selection helps reduce unnecessary input variables and allows the model to focus on features that provide useful information for the classification task.

6. Model Training

A Random Forest Classifier is used for the classification task.

Random Forest is a supervised Machine Learning algorithm that combines multiple decision trees to perform classification.

The model is trained using the selected clinical features from the training dataset.

During training, the model learns patterns associated with the cancer and non-cancer classes.

7. Prediction

After the Random Forest model has been trained, it is used to predict the cancer classification of observations in the testing dataset.

The predicted classes are represented as:

0 → Non-cancer
1 → Cancer
8. Model Evaluation

The performance of the trained model is evaluated using:

Accuracy

Accuracy represents the proportion of observations that were correctly classified by the model.

Confusion Matrix

The confusion matrix shows the number of correct and incorrect predictions for the cancer and non-cancer classes.

Precision

Precision indicates how many of the observations predicted as cancer are actually cancer cases.

Recall

Recall indicates how many of the actual cancer cases were correctly identified by the model.

F1-Score

The F1-score provides a combined measure of precision and recall.

Results

The trained Random Forest model is evaluated using accuracy, confusion matrix, precision, recall, and F1-score.

The complete implementation and generated results are available in the Jupyter Notebook:

lung_cancer_classification.ipynb

Tools and Technologies
Python
Pandas
Scikit-learn
Matplotlib
Google Colab
Jupyter Notebook
Repository Structure
lung-cancer-ml-classification/
│
├── README.md
│
├── lung_cancer_classification.ipynb
│
└── results/
    └── confusion_matrix.png
Project Workflow Summary

This project demonstrates a basic clinical Machine Learning workflow starting from data loading and preprocessing and continuing through feature selection, model training, prediction, and evaluation.

The workflow demonstrates how supervised Machine Learning can be applied to structured clinical data for binary classification.

Important Note

This project is intended for educational and Machine Learning practice purposes.

The model demonstrates classification using a publicly available clinical dataset and should not be considered a clinically validated diagnostic system or used for medical decision-making.

Dataset Attribution

The dataset was obtained from Kaggle:

https://www.kaggle.com/datasets/akashnath29/lung-cancer-dataset

Please refer to the original dataset page for the applicable dataset license and attribution information.

Author

Vinay Kumar Reddy P.

M.Sc. Bioinformatics

Interests: Bioinformatics, Genomics, Machine Learning, Computational Biology

