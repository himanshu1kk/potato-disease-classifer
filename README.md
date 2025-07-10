

PROJECT: Potato Disease Detection using CNN


1. PROBLEM STATEMENT
------------------------------
This project focuses on developing a deep learning model based on Convolutional Neural Networks (CNNs) to categorize potato plant leaf images into three distinct classes:
- Early Blight
- Late Blight
- Healthy

The goal is to enable fast and accurate disease identification through image-based classification, potentially aiding farmers in early disease management.

2. TOOLS AND TECHNOLOGIES UTILIZED
------------------------------
- Programming Language: Python
- Frameworks & Libraries: TensorFlow, Keras, Matplotlib, NumPy
- Dataset Format: Directory-based folder structure with labeled images
- Image Processing: Resized all images to 256x256 pixels
- Batch Size Used: 32
- Dataset Split: 80% Training, 10% Validation, 10% Testing

3. ARCHITECTURE OF THE CNN MODEL
------------------------------
- Input Format: Color images with shape (256, 256, 3)
- Total Input Samples per Batch: 32

Model Layers Overview:
1. Resizing and Rescaling
2. Data Augmentation (Random flipping and rotation)
3. Conv2D Layer → 32 filters, 3x3 kernel, ReLU activation
4. MaxPooling Layer → 2x2
5. Dropout (Rate: 0.2)
6. Conv2D Layer → 64 filters, 3x3, ReLU
7. MaxPooling → 2x2
8. Dropout (0.3)
9. Conv2D Layer → 64 filters, 3x3, ReLU
10. MaxPooling → 2x2
11. Dropout (0.3)
12. Conv2D Layer → 64 filters, 3x3, ReLU
13. MaxPooling → 2x2
14. Dropout (0.3)
15. Conv2D Layer → 64 filters, 3x3, ReLU
16. MaxPooling → 2x2
17. Dropout (0.3)
18. Conv2D Layer → 64 filters, 3x3, ReLU
19. MaxPooling → 2x2
20. Dropout (0.4)
21. Flattening Layer
22. Dense Layer with 64 neurons, ReLU activation, L2 Regularization
23. Final Dense Output Layer with 3 neurons and Softmax activation

Compilation and Training Details:
- Loss Function: Sparse Categorical Crossentropy
- Optimizer: Adam
- Callback Used: EarlyStopping (patience=5, restore_best_weights=True)
- Training Epochs: Up to 50

4. STRATEGIES IMPLEMENTED FOR PERFORMANCE ENHANCEMENT
-------------------------------------------------------
- Data Augmentation: Introduced random flips and rotations for robust training
- Dropout Layers: Prevented overfitting by randomly disabling neurons
- Regularization (L2): Controlled weight magnitudes in dense layers
- Early Stopping: Halted training upon stagnation in validation performance
- Prefetch and Caching: Enhanced training speed and efficiency using TensorFlow’s input pipeline optimizations

5. PERFORMANCE RESULTS AND OUTPUT VISUALIZATION
-------------------------------------------------------
Training Metrics:
- Final Training Accuracy: ~96%
- Final Validation Accuracy: ~96%
- Test Accuracy Achieved: ~97.5% on unseen data

Visualization Components:
- Plotted feature maps from Conv2D layers 1, 4, and 5 to interpret feature learning
- Displayed 10 random test images with actual vs. predicted labels
- Generated plots for training and validation accuracy and loss over epochs to visualize learning trends

6. CONCLUSION
------------------------------
The constructed CNN model demonstrates exceptional capability in detecting and classifying potato leaf diseases across three categories with high accuracy. Regularization, dropout, and augmentation significantly improved the model’s generalization. Feature map visualizations provided insight into learned spatial features, and early stopping helped prevent overfitting by ensuring the model didn’t train longer than necessary. These results indicate strong potential for deploying such models in agricultural disease detection systems.

