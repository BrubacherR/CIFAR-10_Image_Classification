# CIFAR-10_Image_Classification
This project showcases a Convolutional Neural Network (CNN) model designed to classify images from the CIFAR-10 dataset. The model achieves an accuracy of **90%** after 100 epochs of training.

In the code provided, the model is trained for 30 epochs, reaching an accuracy of **87%**. With additional training, the model's performance should improve, peaking at around 90% accuracy after 100 epochs.

#### Dataset:
CIFAR-10 is a widely used dataset for machine learning and computer vision tasks. It consists of **60,000 32x32 color images** in **10 classes**, with 6,000 images per class. The classes represent different objects such as airplanes, cars, birds, cats, deer, dogs, frogs, horses, ships, and trucks. The dataset is divided into **50,000 training images** and **10,000 test images**.

#### Model Architecture:
The CNN model is composed of three convolutional blocks, each followed by ReLU activation and max pooling layers. Batch normalization is applied after the first, second and third convolutional layers to stabilize training and improve convergence. Dropout layers are used to reduce overfitting. The fully connected classifier consists of two dense layers with ReLU activations, followed by a final output layer with 10 units corresponding to the 10 classes in CIFAR-10.

#### Model Layers:
- **Convolutional Blocks:**
  - **Block 1:** Conv(3x3, 32 filters) → BatchNorm → ReLU → Conv(3x3, 64 filters) → ReLU → MaxPool(2x2)
  - **Block 2:** Conv(3x3, 128 filters) → BatchNorm → ReLU → Conv(3x3, 128 filters) → ReLU → MaxPool(2x2) → Dropout(0.05)
  - **Block 3:** Conv(3x3, 256 filters) → BatchNorm → ReLU → Conv(3x3, 256 filters) → ReLU → MaxPool(2x2)
- **Classifier:**
  - Flatten → Dropout(0.1) → Dense(1024) → ReLU → Dense(512) → ReLU → Dropout(0.1) → Dense(10)

#### Results:
- **Initial Training:** 87% accuracy after 30 epochs.
- **Extended Training:** 90% accuracy after 100 epochs.
