# Ensemble Models for Deepfake Detection

This project demonstrates how to train and evaluate ensemble models using base SVM and Deep Feedforward Neural Network (Deep FFNN) models for deepfake detection. The ensemble methods used are Bagging and Boosting.

## Dataset Description

The dataset is structured with separate training and validation directories. Each directory contains subdirectories for different classes (real and fake with specific manipulations).

### Data Annotations

The dataset provides binary labels (real or fake), labels for specific manipulations, and semantics-oriented labels. Examples include:
- **FakeManipulation-1**: Identity
- **FakeManipulation-2**: Identity
- **FakeManipulation-3**: Expression Identity
- **FakeManipulation-4**: Expression Identity
- **FakeManipulation-5**: Expression Head Pose

### Image Details
- **Format**: JPEG
- **Dimensions**: Various, commonly 220x165, 311x230, and 252x252.
- **Resolution**: 220x220

## Ensemble Methods Implemented

### Bagging Ensemble with Base SVM

- **Purpose**: Reduces variance and improves model stability by training multiple SVM models on different subsets of the data.
- **File**: `bagging_ensemble.py`
- **Details**: 
  - Uses `BaggingClassifier` with `SVC` as the base estimator.
  - Utilizes all available CPU cores for training and cross-validation.

### Boosting Ensemble with Base SVM

- **Purpose**: Converts weak learners into strong learners by iteratively training SVM models and focusing on misclassified instances.
- **File**: `boosting_ensemble.py`
- **Details**: 
  - Uses `AdaBoostClassifier` with `SVC` as the base estimator.
  - Utilizes all available CPU cores for training and cross-validation.

## Usage

### Bagging Ensemble with SVM
Run the Bagging ensemble training script:
```sh
python bagging_ensemble.py
