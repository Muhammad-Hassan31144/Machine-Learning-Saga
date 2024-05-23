
### Deep Feedforward Neural Network (Deep FFNN) README

#### `deepffnn_readme.md`

```markdown
# Deep Feedforward Neural Network for Deepfake Detection

This project demonstrates how to train and evaluate a Deep Feedforward Neural Network (Deep FFNN) for deepfake detection using an image dataset.

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

## Model Implementation

### Deep Feedforward Neural Network (Deep FFNN)

- **Purpose**: Captures complex patterns in image data for deepfake detection.
- **File**: `deepffnn_deepfake_detection.py`
- **Details**:
  - Several dense layers with BatchNormalization and Dropout to prevent overfitting.
  - Utilizes all available CPU cores for training and cross-validation.

## Usage

Run the Deep FFNN training script:
```sh
python deepffnn_deepfake_detection.py
