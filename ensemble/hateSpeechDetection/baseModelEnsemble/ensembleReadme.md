# Ensemble Methods for Hate Speech Detection

This project demonstrates how to train and evaluate ensemble models (Bagging and Boosting) for hate speech detection using the `HateSpeechDetection.csv` dataset. The code includes necessary preprocessing steps such as lemmatization and removing stop words.

## Dataset

The dataset is expected to be in CSV format with the following structure:
- **Columns**:
  - `text`: Contains the paragraph text.
  - `label`: Contains the target variable indicating whether the text is hate speech or not.

## Preprocessing

1. **Tokenization and Lemmatization**:
   - Text data is tokenized and lemmatized using NLTK.
   - Stop words are removed to clean the text data.

2. **TF-IDF Vectorization**:
   - Text data is converted into TF-IDF features for model training.

## Bagging (Random Forest)

1. **Load and Preprocess the Dataset**:
   - The dataset is loaded and preprocessed (lemmatization, removing stop words).
   - Text data is vectorized using TF-IDF.

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

1. **Load and Preprocess the Dataset**:
   - The dataset is loaded and preprocessed (lemmatization, removing stop words).
   - Text data is vectorized using TF-IDF.

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
- numpy
- scikit-learn
- joblib
- nltk

## Examples

### Bagging

```sh
python bagging_ensemble.py
