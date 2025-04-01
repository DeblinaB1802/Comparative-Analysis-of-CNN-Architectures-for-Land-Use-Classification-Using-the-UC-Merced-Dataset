# Comparative-Analysis-of-CNN-Architectures-for-Land-Use-Classification-Using-the-UC-Merced-Dataset
1. Introduction
Land use classification plays a crucial role in urban planning, environmental monitoring, and remote sensing applications. Deep learning-based models, particularly Convolutional Neural Networks (CNNs), have demonstrated remarkable capabilities in image classification tasks. This project explores the effectiveness of three well-established CNN architectures — Inception-v1, VGG-19, and ResNet-50 for classifying land use images from the UC Merced Land-Use dataset. A key focus of this study is analysing the performance of each model to understand their strengths and limitations in land use classification.
2. Methodology
2.1 Dataset Overview
The UC Merced Land-Use dataset consists of 2,100 images categorized into 21 land use classes (e.g., residential, agricultural, industrial). Each category contains 100 images of 256×256 resolution. The dataset is split into training and test sets in an 80:20 ratio.
2.2 Data Preprocessing
•	Images are resized to 224×224 for compatibility with CNN architectures.
•	Data augmentation techniques (random rotation, horizontal flipping) are applied to improve model generalization.
•	Pixel values are normalized to the [0,1] range.
2.3 Model Architectures
2.3.1 VGG-19
•	19-layer deep CNN with uniform 3×3 convolutional filters.
•	Fully connected layers at the end for classification.
•	High parameter count leading to increased computational cost.
•	Lacks shortcut connections, making training deeper networks more challenging.
2.3.2 Google-Net (Inception-v1)
•	22-layer deep network with inception modules.
•	Uses multiple kernel sizes to capture spatial hierarchies.
•	Reduces computational complexity while maintaining high accuracy.
2.3.3 ResNet-50
•	50-layer deep residual network with skip connections.
•	Mitigates vanishing gradient problem using residual learning.
•	Uses batch normalization for faster convergence.
•	Deeper architecture allows it to learn complex features but is prone to overfitting.
2.4 Training Procedure
•	Optimizer: Adam optimizer with an initial learning rate of 0.001.
•	Loss Function: Cross-Entropy Loss.
•	Training Epochs: 15 for Google-Net, 35 for VGG-19, and 17 for ResNet-50.
•	Batch Size: 32.
3. Results
3.1 Accuracy Comparison
Model	Test Accuracy
Google-Net (Inception-v1)	82.86%
VGG-19	78.10%
ResNet-50	70.32%
3.2 Confusion Matrices Analysis
•	Google-Net demonstrated superior classification across most categories, achieving high precision and recall.
•	VGG-19 performed moderately well, with strong performance on distinct land use classes but some confusion among similar-looking categories.
•	ResNet-50 exhibited the highest misclassification rates, particularly for visually similar land use types, indicating difficulty in learning discriminative features.
4. Discussion
4.1 Performance Analysis
	Google-Net Performance
Google-Net outperformed the other models due to its efficient use of inception modules, which allow the network to analyse multiple spatial resolutions simultaneously. This multi-scale feature extraction helped distinguish between visually similar land use classes by capturing fine and coarse details in the images. The model's relatively lower parameter count compared to VGG-19 also contributed to a more efficient training process, making it computationally favourable without compromising accuracy.

	VGG-19 Performance
VGG-19, despite achieving reasonably high accuracy, faced significant challenges due to its deep architecture with densely connected layers. The uniform use of 3×3 convolutions allowed it to learn hierarchical representations effectively, but the lack of shortcut connections led to difficulties in optimizing deeper layers. The fully connected layers introduced a large number of parameters, making the model computationally expensive and prone to overfitting. While it performed well on distinct land use categories such as 'runway' and 'golf course,' it struggled with classes that shared similar textures and spatial structures, leading to increased misclassification rates in those areas.
	ResNet-50 Performance
ResNet-50, despite being the deepest model among the three, exhibited the lowest classification accuracy. One key reason for its underperformance was potential overfitting due to the dataset size, as deeper networks generally require larger datasets to fully leverage their depth. The residual connections, while effective in very deep networks, may not have provided significant advantages for this specific classification task, where intermediate feature learning is already sufficient. Another challenge with ResNet-50 was its tendency to misclassify visually similar classes, indicating that it struggled with learning discriminative features effectively.
4.2 Challenges and Improvements
•	Overfitting in ResNet-50: Implementing dropout or L2 regularization techniques may reduce overfitting and improve generalization.
•	Hyperparameter tuning: Adjusting learning rates, batch sizes, and weight decay could lead to improved model performance.
•	Transfer Learning: Using pre-trained models trained on remote sensing datasets may enhance feature extraction for land use classification.
•	Ensemble Learning: Combining predictions from all three models could yield better classification results by leveraging their strengths.
5. Conclusion
This study highlights the effectiveness of different CNN architectures for land use classification. Google-Net outperformed VGG-19 and ResNet-50 due to its efficient feature extraction and depth, while VGG-19 provided a balance between performance and computational cost. ResNet-50, despite its deep architecture, struggled due to potential overfitting and a lack of significant benefits from residual connections in this specific task. Future work may explore fine-tuning hyperparameters, using larger datasets, and integrating domain-specific transfer learning to further enhance performance.

