# Comparative-Analysis-of-CNN-Architectures-for-Land-Use-Classification-Using-the-UC-Merced-Dataset
# UCMerced Land Use Classification with CNNs

## 📌 Project Overview
This project implements and evaluates three popular Convolutional Neural Networks (CNNs)—GoogleNet, VGG-19, and ResNet-50—for land use classification using the **UCMerced Land Use dataset**. The objective is to compare their performance in terms of classification accuracy and identify the most effective architecture for this task.

## 📂 Dataset
- **Name:** UCMerced Land Use Dataset
- **Total Images:** 2,100
- **Categories:** 21 land use classes (e.g., agricultural, commercial, freeway, golf course, residential, etc.)
- **Resolution:** 256×256 pixels per image
- **Train-Test Split:** 70% training, 30% testing

## 🏗️ Model Architectures
The following CNN architectures were implemented and evaluated:
- **GoogleNet (Inception-v1)**: Multi-scale feature extraction with inception modules.
- **VGG-19**: Deep CNN with uniform 3×3 convolutions and fully connected layers.
- **ResNet-50**: Deep residual network with skip connections to improve gradient flow.

## 🚀 Performance Results
| Model      | Test Accuracy |
|------------|--------------|
| **GoogleNet**  | **82.86%**    |
| **VGG-19**     | 78.10%       |
| **ResNet-50**  | 70.32%       |

### Key Findings
- **GoogleNet performed the best**, leveraging inception modules for efficient multi-scale feature extraction.
- **VGG-19 achieved moderate accuracy** but was computationally expensive due to its large number of parameters.
- **ResNet-50 underperformed**, possibly due to overfitting and difficulties in learning discriminative features.

### 4️⃣ Evaluate the Models
Each model's performance is evaluated using accuracy metrics and confusion matrices.

## 📈 Future Improvements
- Fine-tuning hyperparameters for better model generalization and use regularization techniques to avoid overfitting.
- Implementing ensemble learning for improved accuracy.
- Exploring transfer learning using pre-trained models on remote sensing datasets.

## 🤝 Contributing
Contributions are welcome! Feel free to fork the repository and submit a pull request.
---
**Author:** Deblina Biswas



