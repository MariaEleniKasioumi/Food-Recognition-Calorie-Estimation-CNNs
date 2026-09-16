# Food-Recognition-Calorie-Estimation-CNNs

#  Food Recognition & Calorie Estimation using CNNs

##  Overview
This project presents a comprehensive comparative study of Convolutional Neural Network (CNN) architectures for food image recognition and calorie estimation using the **Food-11 dataset**. 

Beyond simple classification, the project introduces two distinct methodologies for calorie estimation: a probabilistic Top-K weighted approach based on USDA data, and a geometric computer vision approach utilizing a reference object (2€ coin)[cite: 3].

##  Key Methodologies & Features
* **Two-Phase Transfer Learning:** Applied frozen feature extraction followed by full fine-tuning using discriminative learning rates to prevent catastrophic forgetting[cite: 3].
* **Handling Class Imbalance:** Integrated a Weighted Cross-Entropy Loss function to effectively train on a dataset with an imbalance ratio of 5.36x (e.g., heavily weighting the minority 'Rice' class)[cite: 3].
* **Data Augmentation:** Implemented targeted transformations (RandomResizedCrop, RandomHorizontalFlip, ColorJitter) mimicking real-world food photography[cite: 3].
* **Calorie Estimation Module:** 
  * *Method A:* Calibrated uncertainty via Top-K weighted softmax predictions[cite: 3].
  * *Method B:* Gram-level precision using geometric pixel-to-cm conversion[cite: 3].

##  Models Evaluated
1. **ResNet50 (Transfer Learning):** Achieved the highest performance.
2. **MobileNetV2 (Transfer Learning):** Explored the efficiency frontier for mobile deployment (10x fewer parameters than ResNet50)[cite: 3].
3. **EfficientNet-B0 (Transfer Learning):** Evaluated NAS-based balanced scaling[cite: 3].
4. **Custom CNN (Baseline):** Trained entirely from scratch (4 conv blocks, Global Average Pooling)[cite: 3].

##  Results Comparison (Test Set)
| Model | Parameters (M) | Test Accuracy | Macro F1-Score |
| :--- | :---: | :---: | :---: |
| **ResNet50** | 23.53 | **90.29%** | **0.9067** |
| **EfficientNet-B0** | 4.02 | 86.29% | 0.8644 |
| **MobileNetV2** | 2.24 | 83.75% | 0.8329 |
| **Custom CNN** | 1.21 | 62.71% | 0.6370 |

*Note: ResNet50 achieved near-perfect recognition on distinct classes (e.g., Soup F1=0.968) and successfully handled complex, highly-variable classes (e.g., Dessert F1=0.859)[cite: 3].*

## 📁 Repository Structure
* `[Name_of_your_notebook].ipynb`: The main Jupyter Notebook containing the data preprocessing, model architectures, training loops, and evaluation metrics.
* `Food-11_Report_Greek.pdf`: The full detailed academic report (in Greek).
* `Food-11_Presentation_Greek.pptx`: Slide deck summarizing the methodology and results.
