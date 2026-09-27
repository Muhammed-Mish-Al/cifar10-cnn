
# CIFAR-10 CNN Image Classification

**Internspot Capstone Project**

A Convolutional Neural Network (CNN) built with TensorFlow/Keras to classify images from the CIFAR-10 dataset into 10 different categories.

This project was completed as part of my **Internspot Capstone Project**, where I worked through the complete process of building, training, and evaluating an image classification model.

## Overview

The project follows a complete deep learning workflow:

```text
Load Dataset
     ↓
Explore Data
     ↓
Preprocess Images
     ↓
Train / Validation Split
     ↓
Encode Labels
     ↓
Build CNN
     ↓
Train Model
     ↓
Evaluate Model
     ↓
Generate Predictions
     ↓
Analyze Results
```

The model works with 32×32 RGB images and classifies them into the following CIFAR-10 categories:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## Model Architecture

The CNN used in this project consists of three convolutional layers followed by fully connected layers:

```text
Input (32×32×3)
        ↓
Conv2D (32 filters, 3×3)
        ↓
MaxPooling2D (2×2)
        ↓
Conv2D (64 filters, 3×3)
        ↓
MaxPooling2D (2×2)
        ↓
Conv2D (64 filters, 3×3)
        ↓
Flatten
        ↓
Dense (64 neurons)
        ↓
Dense (10 neurons, Softmax)
```

The convolutional layers are used to learn visual patterns from the images, while max pooling reduces the spatial dimensions of the feature maps. The final softmax layer produces probabilities for each of the 10 classes.

## Dataset

This project uses the **CIFAR-10 dataset** through TensorFlow/Keras.

- 50,000 training images
- 10,000 test images
- Image size: 32×32 pixels
- Image type: RGB
- Number of classes: 10

The original training data is further divided into:

- 80% training data
- 20% validation data

The image pixel values are normalized from the original `0–255` range to `0–1` before training.

## Training

The model was trained using:

- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Metric:** Accuracy
- **Epochs:** 15
- **Batch Size:** 64

## Evaluation

After training, the model is evaluated using the separate CIFAR-10 test set.

The project includes:

- Test accuracy and loss
- Training vs. validation accuracy
- Training vs. validation loss
- Sample predictions
- Confusion matrix

The confusion matrix is used to see which classes the model predicts well and which classes it tends to confuse with each other.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
cifar10-cnn/
│
├── image_classification.ipynb
└── README.md
```

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Muhammed-Mish-Al/cifar10-cnn.git
cd cifar10-cnn
```

### 2. Install the required libraries

```bash
pip install numpy matplotlib tensorflow scikit-learn jupyter
```

### 3. Open the notebook

```bash
jupyter notebook image_classification.ipynb
```

Run the notebook cells from top to bottom.

## Results

The notebook provides:

- Sample images from the CIFAR-10 dataset
- Training and validation accuracy plots
- Training and validation loss plots
- Test-set predictions
- Confusion matrix
- Final test accuracy

The results can be used to understand both the overall performance of the model and the classes that are more difficult for the CNN to distinguish.

## What I Learned

This project helped me get more comfortable with the basic workflow involved in building an image classification model.

Some of the main concepts I worked with were:

- Loading and exploring image datasets
- Image preprocessing and normalization
- NumPy arrays and image tensors
- Convolutional neural networks
- Convolution and pooling layers
- ReLU and Softmax activation functions
- One-hot encoding
- Training and validation
- Adam optimization
- Categorical crossentropy
- Model evaluation
- Making predictions
- Confusion matrix analysis

## Future Plans

The next step for this project is to improve the current CNN model and compare it with the existing 68.10% baseline.

The planned improvements(as time permits) include:

- Build a CNN V2 with data augmentation
- Add batch normalization and dropout
- Experiment with the CNN architecture and training parameters
- Compare CNN V2 with the current model
- Analyze whether the improvements help with difficult classes such as cats, dogs and birds

The goal is to improve the model's generalization and achieve better performance while understanding how each change affects the results.
