# Brain Tumor Detection (Semantic Segmentation)

This repository contains a deep learning project for detecting brain tumors using semantic segmentation. The model is trained using TensorFlow and Keras with the COCO dataset format for annotations.

## Features
- Uses **DeepLabV3+** with a **ResNet-50** backbone for segmentation.
- Dataset is processed from COCO format with masks and images.
- Supports visualization of dataset samples and model predictions.
- Implements **data preprocessing** including resizing and normalization.

## Installation

## Dataset
- The dataset consists of MRI scans annotated for brain tumors.
- It is structured as:
  ```
  dataset/
  |-- train/
  |   |-- images/
  |   |-- _annotations.coco.json
  |-- valid/
  |   |-- images/
  |   |-- _annotations.coco.json
  |-- test/
  |   |-- images/
  |   |-- _annotations.coco.json
  ```

## Model Training
1. Train the model:
   ```python
   python train.py
   ```
2. Evaluate on test data:
   ```python
   python evaluate.py
   ```

## Model Saving & Loading
- Save the trained model:
  ```python
  model.save("brain_tumor_segmentation.h5")
  ```
- Load a saved model:
  ```python
  from tensorflow.keras.models import load_model
  model = load_model("brain_tumor_segmentation.h5")
  ```

## Visualization
- **Dataset Visualization**:
  ```python
  visualize_dataset(train_dataset)
  ```
- **Model Predictions**:
  ```python
  visualize_predictions(model, test_dataset)
  ```

## Contributing
Feel free to fork this repository and contribute improvements.

## License
This project is licensed under the MIT License.

