# Food-Recognition-Calorie-Estimation-CNNs

## Food-11 Dataset Analysis
* Conducted a comparative study of Convolutional Neural Networks (Custom CNN, ResNet50, MobileNetV2, EfficientNet-B0) for food image recognition.
* Implemented a two-phase transfer learning strategy (frozen feature extraction and full fine-tuning) using discriminative learning rates.
* Handled severe class imbalance (5.36x ratio) by integrating a Weighted Cross-Entropy Loss function.
* Applied targeted data augmentation techniques (RandomResizedCrop, ColorJitter, RandomRotation) to simulate real-world food photography.
* Developed a calorie estimation module using a probabilistic Top-K weighted approach based on USDA nutritional data.
* Implemented an alternative geometric calorie estimation method utilizing a reference object (2€ coin) for pixel-to-cm conversion.
* Evaluated models using Accuracy and Macro F1-Score, achieving a peak accuracy of 90.29% with ResNet50.
