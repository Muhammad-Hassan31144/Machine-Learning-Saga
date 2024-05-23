
### README for Deep Feedforward Neural Network (MLP)

#### `deepfeedforward_readme.md`

```markdown
# Deep Feedforward Neural Network for IoT Intrusion Detection

This project demonstrates how to train and evaluate a Deep Feedforward Neural Network (MLP) for IoT Intrusion Detection using the `IoT_Intrusion.csv` dataset. The code leverages full CPU utilization during training.

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

3. **Preprocess the Data**:
   - One-hot encoding is applied to the target variable.

4. **Build the Neural Network Model**:
   - A sequential neural network model is built with two hidden layers.

5. **Train the Model**:
   - The model is trained using the training data.
   - Full CPU utilization is configured in TensorFlow.

6. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

7. **Save the Model**:
   - The trained model is saved to a file for later use.

## Usage

Run the provided Python script to train and evaluate the Deep Feedforward Neural Network model. Ensure that the dataset is available at the specified file path.

## Requirements

- pandas
- numpy
- tensorflow
- scikit-learn

## Example

```sh
python deepfeedforward_model.py
