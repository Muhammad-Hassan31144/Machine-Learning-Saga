# SVM Model for Deepfake Detection (Image Dataset)

This project demonstrates how to train and evaluate a Support Vector Machine (SVM) model for deepfake detection using an image dataset. The dataset is structured with separate training and validation directories. The code leverages full CPU utilization during training and cross-validation.


- **train**: Directory containing training images, organized by class.
- **val**: Directory containing validation images, organized by class.

## Preprocessing

1. **Image Loading and Resizing**:
   - Images are loaded recursively from the directory structure.
   - Images are converted to grayscale and resized to a consistent dimension (220x220).

2. **Flattening**:
   - Resized images are flattened into one-dimensional arrays for SVM input.

## Model

1. **Classifier**: Support Vector Machine (SVM) with RBF kernel
   - **Reason**: SVMs are effective for image classification tasks, especially with high-dimensional data like pixel values. They can capture complex patterns using appropriate kernels.

## Steps

1. **Load and Preprocess the Dataset**:
   - The dataset is loaded from the specified directories.
   - Images are preprocessed (resized, converted to grayscale, and flattened).

2. **Encode Labels**:
   - Labels are encoded using `LabelEncoder`.

3. **Train the SVM Model**:
   - The SVM model is trained using full CPU power by utilizing `joblib.Parallel` and `multiprocessing.cpu_count()`.

4. **Cross-Validation**:
   - Cross-validation is performed to evaluate the model's performance on the training data.

5. **Evaluate the Model**:
   - The model is evaluated on the validation data using various metrics (accuracy, precision, recall, F1-score).

6. **Save the Model**:
   - The trained SVM model is saved to a file (`.pkl` for SVM models).

## Usage

Run the provided Python script to train and evaluate the SVM model. Ensure that the dataset is available at the specified file paths.

## Requirements

- pandas
- numpy
- scikit-learn
- joblib
- opencv-python (cv2)

## Example

```sh
python svm_images.py
