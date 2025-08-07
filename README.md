## Agricultural Crops Image Classification

### Project Overview

This project focuses on the task of **classifying agricultural crops from images**. By leveraging a deep learning approach with a pre-trained convolutional neural network, the goal is to build an automated system that can accurately identify different types of crops. This technology can be a valuable tool for modern agriculture, enabling efficient monitoring and management of crops.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Agricultural Crops Image Classification](https://www.kaggle.com/datasets/mdwaquarazam/agricultural-crops-image-classification)
  * **Size**: The dataset contains 829 images categorized into 30 classes. It's split into a training set of 663 images, and validation and test sets of 83 images each.
  * **Key Features**: The raw image data is used as input for the model.
  * **Approach**:
      * **Data Preparation**: The images are loaded and organized into a DataFrame.
      * **Data Augmentation**: Techniques like horizontal flipping, rotation, zooming, and brightness adjustments are applied to the training images to increase the size and diversity of the dataset, which helps prevent overfitting.
      * **Transfer Learning**: A pre-trained `EfficientNetB3` model, which was trained on a large image dataset (ImageNet), is used as a feature extractor.
      * **Model Architecture**: A custom deep learning model is built on top of the pre-trained EfficientNetB3 base, featuring `BatchNormalization`, `Flatten`, and several `Dense` layers with `Dropout` for regularization and classification.
      * **Training**: The model is trained using the Adam optimizer with `categorical_crossentropy` as the loss function.
  * **Best Performance**:
      * The model achieved a final validation accuracy of **71.1%**.
      * The model showed good learning progression, as visualized by the training and validation accuracy and loss plots.

-----

### Purpose and Applications

  * **Automated Crop Identification**: Automatically classify crops from aerial or on-the-ground imagery.
  * **Crop Monitoring**: Help farmers and agronomists monitor crop health and growth without manual inspection.
  * **Precision Agriculture**: Enable data-driven decisions on resource allocation, such as water and fertilizer, based on crop type and health.
  * **Yield Prediction and Disease Detection**: Serve as a foundational step for more complex tasks like predicting crop yield or detecting plant diseases.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Agricultural-Crops-Image-Classification-Using-CNN.git
cd Agricultural-Crops-Image-Classification-Using-CNN
```

Install the necessary libraries:

```bash
pip install tensorflow keras pandas numpy seaborn matplotlib scikit-learn opencv-python
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Exploring different pre-trained models like `ResNet50`, `MobileNetV2`, or `InceptionV3` to find a more suitable architecture.
  * Implementing a learning rate scheduler and callbacks for more effective training.
  * Performing more extensive data augmentation and hyperparameter tuning to boost the model's accuracy.
  * Fine-tuning the entire model, rather than just the top layers, to potentially achieve better performance.
