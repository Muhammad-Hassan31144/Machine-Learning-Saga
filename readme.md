# Machine Learning Models for Various Datasets

This project demonstrates the application of various machine learning models on three different types of datasets: numeric, text, and image. The primary goal is to evaluate and compare the performance of different classifiers, ensemble methods, and deep feedforward neural networks (DeepFFNN) on each dataset type. Cross-validation is implemented for all models to ensure robust performance evaluation.

## Datasets

### 1. IoT Intrusion Detection (Numeric)
- **Dataset**: `IoT_Intrusion.csv`
- **Features**: Numeric features representing various attributes of network traffic.
- **Target Variable**: Binary label indicating whether the network traffic is normal or an intrusion.
- **Chosen Classifier**: Support Vector Machine (SVM)
  - **Reason**: SVM is effective in high-dimensional spaces and is widely used for binary classification tasks. It works well with numeric data and can handle non-linear relationships using kernel functions.

### 2. Hate Speech Detection (Text)
- **Dataset**: `HateSpeechDetection.csv`
- **Features**: Text data containing paragraphs.
- **Target Variable**: Binary label indicating whether the text is hate speech or not.
- **Chosen Classifier**: Decision Tree (DT)
  - **Reason**: Decision Trees are simple yet powerful models for text classification. They are interpretable and can handle categorical data well after text preprocessing steps like lemmatization and stop word removal.

### 3. Deepfake Detection (Images)
- **Dataset**: `deepfake.zip`
- **Features**: Images of faces with binary labels indicating whether they are real or deepfake.
- **Target Variable**: Binary label indicating the authenticity of the face.
- **Chosen Classifier**: Support Vector Machine (SVM)
  - **Reason**: SVMs are effective for image classification tasks, especially with high-dimensional data like pixel values. They can capture complex patterns using appropriate kernels.

## Models Implemented

### 1. Base Classifiers
- **Numeric (IoT Intrusion Detection)**: SVM
- **Text (Hate Speech Detection)**: Decision Tree
- **Image (Deepfake Detection)**: SVM

### 2. Deep Feedforward Neural Network (DeepFFNN)
- Implemented for all datasets to leverage the power of deep learning in capturing complex patterns and relationships in data.

### 3. Ensemble Methods
- **Bagging (Random Forest)**: Applied to all datasets to reduce variance and improve model stability.
- **Boosting (Gradient Boosting)**: Applied to all datasets to improve model performance by converting weak learners into strong learners.

### 4. Cross-Validation
- Implemented for all models to ensure robust performance evaluation and to prevent overfitting.

## Usage

To run the scripts for training and evaluating the models, ensure that the datasets are available at the specified file paths. Each notebook and script is designed to preprocess the data, train the model, perform cross-validation, and evaluate the model using various metrics.

