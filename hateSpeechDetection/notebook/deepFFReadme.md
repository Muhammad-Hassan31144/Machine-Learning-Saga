
### README for Deep Feedforward Neural Network (MLP)

#### `notebooks/deepfeedforward_readme.md`

```markdown
# Deep Feedforward Neural Network for Hate Speech Detection

This project demonstrates how to train and evaluate a Deep Feedforward Neural Network (MLP) for hate speech detection using the `HateSpeechDetection.csv` dataset. The code includes necessary text preprocessing steps such as lemmatization and stop word removal, and leverages full CPU utilization during training.

## Dataset

The dataset is expected to be in CSV format with the following structure:
- **Features**: The column named `text` contains the text data.
- **Target Variable**: The column named `label` contains the target variable indicating hate speech.

## Steps

1. **Load the Dataset**:
   - The dataset is loaded from a local file path.
   - Features and target variables are separated.

2. **Preprocess the Text Data**:
   - The text data is preprocessed by removing stop words and applying lemmatization.

3. **Convert Text to TF-IDF Features**:
   - The text data is transformed into TF-IDF features.

4. **Split the Data**:
   - The data is split into training and testing sets using an 80-20 split.

5. **One-hot Encode the Labels**:
   - The target labels are one-hot encoded for use with the neural network.

6. **Build the Neural Network Model**:
   - A sequential neural network model is built with two hidden layers.

7. **Train the Model**:
   - The model is trained using the training data.
   - Full CPU utilization is configured in TensorFlow.

8. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

9. **Save the Model**:
   - The trained model is saved to a file for later use.

## Usage

Run the provided Python script to train and evaluate the Deep Feedforward Neural Network model. Ensure that the dataset is available at the specified file path.

## Requirements

- pandas
- numpy
- nltk
- tensorflow
- scikit-learn

## Example

```sh
python deepfeedforward_model.py
