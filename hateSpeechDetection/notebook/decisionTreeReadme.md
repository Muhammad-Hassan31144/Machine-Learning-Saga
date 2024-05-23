# Decision Tree Model for Hate Speech Detection

This project demonstrates how to train and evaluate a Decision Tree model for hate speech detection using the `HateSpeechDetection.csv` dataset. The code includes necessary text preprocessing steps such as lemmatization and stop word removal.

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

5. **Train the Decision Tree Model**:
   - A Decision Tree model is trained using the training data.

6. **Cross-Validation**:
   - Cross-validation is performed to evaluate the model's performance on the training data.

7. **Evaluate the Model**:
   - The model is evaluated on the test data using various metrics (accuracy, precision, recall, F1-score).

8. **Save the Model**:
   - The trained Decision Tree model is saved to a file for later use.

## Usage

Run the provided Python script to train and evaluate the Decision Tree model. Ensure that the dataset is available at the specified file path.

## Requirements

- pandas
- nltk
- scikit-learn
- joblib

## Example

```sh
python dt_model.py
