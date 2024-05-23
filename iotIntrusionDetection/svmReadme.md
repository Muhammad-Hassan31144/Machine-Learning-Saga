# SVM Model for IoT Intrusion Detection

This project demonstrates how to train and evaluate a Support Vector Machine (SVM) model for IoT Intrusion Detection using the `IoT_Intrusion.csv` dataset. The code leverages full CPU utilization during training and cross-validation.

## Dataset

The dataset is expected to be in CSV format with the following structure:
- **Features**: All columns except the last one are used as features.
- **Target Variable**: The last column (`label`) is used as the target variable.

## Steps

1. **Load the Dataset**:
   - The dataset is loaded from a local file path.
   - Features and target variables are separated.

2. **Split the Data**:
   - The data is split into training and testing sets using an 80-20 split.

3. **Train the SVM Model**:
   - An SVM model with an RBF kernel is trained using the training data.
   - Full CPU utilization is achieved by setting `n_jobs=-1` during cross-validation.

4. **Cross-Validation**:
   - Cross-validation is performed to evaluate the model's performance on the training data.

5. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

6. **Save the Model**:
   - The trained SVM model is saved to a file for later use.

## Usage

Run the provided Python script to train and evaluate the SVM model. Ensure that the dataset is available at the specified file path.

## Requirements

- pandas
- scikit-learn
- joblib

## Example

```sh
python svm_model.py
