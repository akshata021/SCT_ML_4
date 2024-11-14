This is hand gesture recognition project, using a pre-trained model (MobileNetV2) as a base model for transfer learning. Here’s a breakdown of the main components:

Dataset Download and Setup:

The dataset, sourced from Kaggle (gti-upm/leapgestrecog), contains images of hand gestures.
Data Augmentation:

The images are preprocessed with augmentations like rotation, width/height shifts, shearing, zooming, and horizontal flipping to improve model robustness.
The dataset is split into training and validation subsets.
Model Setup:

The model is built on the MobileNetV2 architecture, excluding the top classification layer, and adding custom layers for gesture classification.
The model is compiled with categorical cross-entropy as the loss function, and accuracy as a performance metric.
Training and Fine-Tuning:

Initial training is conducted with frozen base layers.
Fine-tuning then allows for training of all layers with a lower learning rate for improved performance.
Model Evaluation and Visualization:

A function is defined to plot accuracy and loss for both training and validation sets.
This visualization is used to assess the model's learning progress.
Model Saving:

Finally, the trained model is saved for later use in predicting hand gestures.
