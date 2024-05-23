
### README for Ensemble Methods

#### `ensemble_readme.md`

```markdown
# Ensemble Methods for IoT Intrusion Detection

This project demonstrates how to train and evaluate ensemble models for IoT Intrusion Detection using the `IoT_Intrusion.csv` dataset. The code includes implementations of Bagging (Random Forest) and Boosting (Gradient Boosting) methods, leveraging full CPU utilization during training and cross-validation.

## Dataset

The dataset is expected to be in CSV format with the following structure:
- **Features**: All columns except the last one are used as features.
- **Target Variable**: The last column (`label`) is used as the target variable.

## Bagging (Random Forest)

1. **Load the Dataset**:
   - The dataset is loaded from a local file path.
   - Features and target variables are separated.

2. **Split the Data**:
   - The data is split into training and testing sets using an 80-20 split.

3. **Train the Random Forest Model**:
   - A Random Forest model is trained using the training data.
   - Full CPU utilization is achieved by setting `n_jobs=-1`.

4. **Cross-Validation**:
   - Cross-validation is performed to evaluate the model's performance on the training data.

5. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

6. **Save the Model**:
   - The trained Random Forest model is saved to a file for later use.

## Boosting (Gradient Boosting)

1. **Load the Dataset**:
   - The dataset is loaded from a local file path.
   - Features and target variables are separated.

2. **Split the Data**:
   - The data is split into training and testing sets using an 80-20 split.

3. **Train the Gradient Boosting Model**:
   - A Gradient Boosting model is trained using the training data.
   - Full CPU utilization is achieved by setting `n_jobs=-1`.

4. **Cross-Validation**:
   - Cross-validation is performed to evaluate the model's performance on the training data.

5. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

6. **Save the Model**:
   - The trained Gradient Boosting model is saved to a file for later use.

## Usage

Run the provided Python scripts to train and evaluate the ensemble models. Ensure that the dataset is available at the specified file path.

## Requirements

- pandas
- scikit-learn
- joblib

## Examples

### Bagging

```sh
python bagging_ensemble.py
