
# Credit Approval Prediction Model

## Overview

This repository contains a machine learning model designed to predict credit approval based on various customer attributes. The model uses a Decision Tree Classifier to classify whether a customer's credit application is approved or denied, based on features such as age, job type, marital status, and more.

## Dataset

The dataset used for training and evaluation is `Credit.csv`, which includes customer information and credit approval status. The dataset has been preprocessed to encode categorical variables into numerical formats suitable for machine learning algorithms.

### Features

- **age:** Age of the customer
- **job:** Type of job the customer holds
- **marital:** Marital status of the customer
- **education:** Level of education of the customer
- **balance:** Account balance of the customer
- **housing:** Whether the customer has a housing loan
- **duration:** Duration of the last contact with the customer
- **campaign:** Number of contacts performed during this campaign

### Target

- **approval:** Indicates if the credit application was approved (`0` for no, `1` for yes)

## Data Preprocessing

Categorical variables were encoded using `LabelEncoder` from scikit-learn:

- **Approval:** Encoded as `0` (no) and `1` (yes)
- **Marital Status:** Encoded as `0` (divorced), `1` (married), `2` (single), and `3` (unknown)
- **Education Level:** Encoded as `0` (primary), `1` (secondary), `2` (tertiary), `3` (unknown), and `4` (nan)
- **Housing Loan:** Encoded as `0` (no), `1` (yes), and `2` (nan)
- **Job Type:** Encoded into 12 categories with `0` for admin, `1` for blue-collar, and so on

## Model Training

### Model Type

- **Classifier:** Decision Tree Classifier

### Training Process

- **Training Set:** 80% of the data
- **Test Set:** 20% of the data
- **Evaluation Metric:** Accuracy

The model was trained on the processed dataset and achieved an accuracy of approximately 86.08% on the test set.

### Performance

- **Accuracy Score:** 0.8608

## Sample Prediction

To demonstrate the model's functionality, a sample test case was used:
- **Input:** `[25.0, 2, 1, 2, 221, 0, 57.0, 2]`
- **Prediction:** `0` (not approved)
