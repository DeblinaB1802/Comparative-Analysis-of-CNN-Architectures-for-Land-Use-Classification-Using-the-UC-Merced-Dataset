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
- Each model's performance is evaluated on - 1) Classification Report , 2) Confusion Matrix

### 4️⃣ Accuracy Analysis
| Model      | Test Accuracy |
|------------|--------------|
| **GoogleNet**  | **82.86%**    |
| **VGG-19**     | 78.10%       |
| **ResNet-50**  | 70.32%       |

### 4️⃣ Confusion Matrix Analysis
- Google-Net demonstrated superior classification across most categories, achieving high precision and recall.
-	VGG-19 performed moderately well, with strong performance on distinct land use classes but some confusion among similar-looking categories.
-	ResNet-50 exhibited the highest misclassification rates, particularly for visually similar land use types, indicating difficulty in learning discriminative features.

### Key Findings
- **GoogleNet performed the best**
- Google-Net outperformed the other models due to its efficient use of inception modules, which allow the network to analyse multiple spatial resolutions simultaneously. This multi-scale feature extraction helped distinguish between visually similar land use classes by capturing fine and coarse details in the images. The model's relatively lower parameter count compared to VGG-19 also contributed to a more efficient training process, making it computationally favourable without compromising accuracy.
- **VGG-19 achieved moderate accuracy**
- VGG-19, despite achieving reasonably high accuracy, faced significant challenges due to its deep architecture with densely connected layers. The uniform use of 3×3 convolutions allowed it to learn hierarchical representations effectively, but the lack of shortcut connections led to difficulties in optimizing deeper layers. The fully connected layers introduced a large number of parameters, making the model computationally expensive and prone to overfitting. While it performed well on distinct land use categories such as 'runway' and 'golf course,' it struggled with classes that shared similar textures and spatial structures, leading to increased misclassification rates in those areas.
- **ResNet-50 underperformed**
- ResNet-50, despite being the deepest model among the three, exhibited the lowest classification accuracy. One key reason for its underperformance was potential overfitting due to the dataset size, as deeper networks generally require larger datasets to fully leverage their depth. The residual connections, while effective in very deep networks, may not have provided significant advantages for this specific classification task, where intermediate feature learning is already sufficient. Another challenge with ResNet-50 was its tendency to misclassify visually similar classes, indicating that it struggled with learning discriminative features effectively.

## 📈 Future Improvements
- Fine-tuning hyperparameters for better model generalization and use regularization techniques to avoid overfitting.
- Implementing ensemble learning for improved accuracy.
- Exploring transfer learning using pre-trained models on remote sensing datasets.

### Conclusion
- This study highlights the effectiveness of different CNN architectures for land use classification. Google-Net outperformed VGG-19 and ResNet-50 due to its efficient feature extraction and depth, while VGG-19 provided a balance between performance and computational cost. ResNet-50, despite its deep architecture, struggled due to potential overfitting and a lack of significant benefits from residual connections in this specific task. Future work may explore fine-tuning hyperparameters, using larger datasets, and integrating domain-specific transfer learning to further enhance performance.

## 🤝 Contributing
Contributions are welcome! Feel free to fork the repository and submit a pull request.
---
**Author:** Deblina Biswas



