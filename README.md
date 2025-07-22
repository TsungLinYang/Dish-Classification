# Overview
This project focuses on classifying images of school lunches served in Taiwanese elementary and junior high schools. It covers 50 common dish categories using deep learning. The final classification is made by averaging the softmax probabilities from both ResNet50 and DenseNet121 (Soft Voting), improving robustness and accuracy.

##  Model Architecture

- ResNet50 (pre-trained on ImageNet)
- DenseNet121 (pre-trained on ImageNet)
- Soft Voting: combines predictions from both models by averaging softmax probabilities

> If the models predict different classes, the average softmax probabilities are used to make the final decision.



##  Training Settings

- Image Size: `(300, 300, 3)`
- Batch Size: `8`
- Epochs: `15`
- Optimizer: `Adam (lr=1e-4)`
- Loss Function: `categorical_crossentropy`
- Augmentation: Rotation, Zoom, Flip, Shift, Shear, etc.

##  Evaluation Metrics

-  **Top-1 Accuracy (Soft Voting):** `79.11%`
-  **Top-5 Accuracy:** `97.15%`
  ![Confusion Matrix]([https://i.imgur.com/abc123.png](https://github.com/TsungLinYang/Dish-Classification/blob/main/confusion_matrix.png))


  
