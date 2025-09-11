# PetSegmentationUNet 🐾

Welcome to **PetSegmentationUNet**! This project implements a U-Net
model for semantic segmentation of pet images using the Oxford-IIIT Pet
dataset 📷. It segments images into three classes: pet, background, and
border, with robust preprocessing, training, and evaluation using IoU
and ROC curves 📊. Perfect for computer vision enthusiasts! 🚀

## 📋 Table of Contents

-   Overview
-   Features
-   Installation
-   Usage
-   Results
-   Contributing
-   License

## 🌟 Overview

This project leverages a U-Net architecture to perform pixel-wise
segmentation on the Oxford-IIIT Pet dataset, which contains images of
cats and dogs with corresponding segmentation masks 🐶🐱. The pipeline
includes data preprocessing, model training, evaluation with IoU and ROC
curves, and visualization of results.

## ✨ Features

-   🖼️ **Data Preprocessing**: Resizes images and masks to 128x128,
    normalizes images, and adjusts mask labels.
-   🧠 **U-Net Model**: A deep U-Net with encoder-decoder architecture
    for accurate segmentation.
-   📊 **Evaluation**: Computes IoU scores and ROC curves for each class
    (pet, background, border).
-   🖌️ **Visualization**: Displays input images, ground truth masks, and
    predicted masks.
-   💾 **Model Saving**: Saves the trained model in HDF5 format.

## 🛠️ Installation

1.  **Clone the Repository**:

    ``` bash
    git clone https://github.com/shervinnd/PetSegmentationUNet.git
    cd PetSegmentationUNet
    ```

2.  **Install Dependencies**: Ensure Python 3.8+ is installed, then run:

    ``` bash
    pip install tensorflow tensorflow-datasets numpy matplotlib scikit-learn
    ```

3.  **Verify TensorFlow**:

    ``` python
    import tensorflow as tf
    print(tf.__version__)
    ```

## 🚀 Usage

1.  **Run the Pipeline**: Execute the scripts in order (provided as
    separate Python files):

    -   `01_load_dataset.py`: Load the Oxford-IIIT Pet dataset 📂.
    -   `02_preprocess_dataset.py`: Preprocess images and masks 🖼️.
    -   `03_unet_model.py`: Define and compile the U-Net model 🧠.
    -   `04_train_model.py`: Train the model for 10 epochs 🎓.
    -   `05_evaluate_visualize.py`: Evaluate and visualize predictions
        📊.
    -   `06_calculate_iou_roc.py`: Compute IoU and ROC curves 📈.
    -   `07_save_model.py`: Save the trained model 💾.

    Run each script:

    ``` bash
    python 01_load_dataset.py
    python 02_preprocess_dataset.py
    # ... and so on
    ```

2.  **Expected Output**:

    -   Model summary with \~31M parameters.
    -   Training logs with loss and accuracy.
    -   Test accuracy and IoU scores per class (pet, background,
        border).
    -   ROC curves with AUC scores for each class.
    -   Visualizations of images, masks, and predictions.

## 📈 Results

-   **Dataset**: Oxford-IIIT Pet with 3680 training and 3669 test
    images.
-   **Model**: U-Net with 3 output classes (pet, background, border).
-   **Metrics**:
    -   IoU scores (example): `[0.6, 0.8, 0.4]` for pet, background,
        border.
    -   ROC AUC scores (example): `[0.85, 0.90, 0.70]` for each class.
-   **Visualizations**: Sample images, ground truth masks, and predicted
    masks displayed in a 3x3 grid.

## 🤝 Contributing

Contributions are welcome! 🌟 To contribute:

1.  Fork the repository.
2.  Create a feature branch (`git checkout -b feature`).
3.  Commit changes (`git commit -m`).
4.  Push to the branch (`git push origin feature`).
5.  Open a Pull Request.

Suggestions for improvement:

-   Add data augmentation 📸.
-   Implement weighted loss for class imbalance ⚖️.
-   Experiment with deeper architectures or learning rate schedules ⏳.

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for
details.\
\
***Powerd by Miracle⚡***
