# Emotion Recognition using ResNet50 + GRU

## Overview
This project implements a deep learning-based facial emotion recognition system using a hybrid architecture combining **ResNet50** and **GRU (Gated Recurrent Unit)** layers. The model is trained to classify facial expressions into multiple emotion categories using the **CK+ dataset**.

The system uses transfer learning with ResNet50 for feature extraction and GRU layers to capture temporal feature relationships, improving classification performance.

## Dataset
The model was trained and evaluated using the **CK+ (Extended Cohn-Kanade) dataset**, which contains labeled facial expression images.

Emotion classes used:
- Anger
- Contempt
- Disgust
- Fear
- Happy
- Sadness
- Surprise

Dataset distribution:
- Training Images: 873
- Testing Images: 203
- Number of Classes: 7

## Model Architecture
The proposed model uses a hybrid deep learning architecture:

1. **ResNet50 (Pretrained on ImageNet)**
   - Used for deep feature extraction from facial images.

2. **Global Average Pooling**
   - Reduces spatial dimensions of feature maps.

3. **Dense Layer**
   - Adds non-linear representation learning.

4. **GRU Layer**
   - Captures sequential relationships between extracted features.

5. **Concatenation Layer**
   - Combines ResNet and GRU feature representations.

6. **Softmax Output Layer**
   - Predicts the emotion class.

## Training Details
- Image Size: 224 × 224
- Batch Size: 32
- Epochs: 50
- Optimizer: Adam
- Loss Function: Categorical Crossentropy

Data augmentation techniques used:
- Rotation
- Horizontal Flip
- Vertical Flip
- Zoom
- Shear

## Results
Model performance on the test dataset:

| Metric | Score |
|------|------|
Accuracy | 95.56% |
Precision | 94.58% |
Recall | 96.05% |
F1 Score | 95.07% |

The model demonstrates strong performance in recognizing facial expressions across multiple emotion classes.

## Evaluation
The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix Visualization

The confusion matrix helps analyze prediction performance across different emotion categories.

## Technologies Used
- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

## Future Improvements

-Train on larger facial emotion datasets such as FER2013

-Improve model generalization using advanced augmentation

-Deploy the model in a real-time emotion recognition application

-Integrate webcam-based real-time prediction


