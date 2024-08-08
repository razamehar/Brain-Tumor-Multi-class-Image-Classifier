# Brain Tumor 3-Way Image Classifier

## Project Overview
In this deep learning project, we developed a robust system to classify brain MRI scans into four categories: glioma tumor, meningioma tumor, pituitary tumor, or no tumor. Addressing the challenge of class imbalance, we employed the undersampling technique. Additionally, we enhanced our dataset through data augmentation techniques, including rotation, width shifting, height shifting, shearing, zooming, and horizontal flipping.

## Images Visualization
<div><b>Five Random Images from each Class</b></div>

<div>
  <img src='docs/review_images1.png'>
</div>

## Methodologies Applied
We adopted three distinct approaches for image classification and compared their performance on our dataset.

### First Approach:
Multi-Layer Convolutional Neural Network (CNN): Our initial model utilized a multi-layer CNN architecture. The layers included convolutional, pooling, and fully connected layers, each contributing to the model's ability to detect and learn intricate patterns and features in the MRI images. We employed regularization through Dropout to handle overfitting. This structure allowed the model to progressively capture low-level features like edges and textures and then combine these into high-level features representing different tumor types.

### Transfer Learning:
We employed transfer learning, a technique where a pre-trained model is used as the starting point for a new task. This method leverages the knowledge gained from large datasets to enhance the learning process on smaller, task-specific datasets.

InceptionV3, originally developed by Google for the ImageNet competition, is a deep convolutional neural network that features inception modules. Inception modules work by employing multiple convolution filters of different sizes simultaneously to capture features at multiple scales within the same layer. These modules capture multi-scale features (low level to high level) through parallel convolutional operations of different sizes, making the model highly effective at recognizing complex patterns.

- Second Model: Feature Extraction with InceptionV3: We used the pre-trained weights from InceptionV3 to extract high-level features from the MRI images. This approach leverages the general image recognition capabilities of InceptionV3 to improve classification accuracy without training a model from scratch.

- Third Model: Fine-Tuning InceptionV3: In this model, we fine-tuned InceptionV3 by adjusting and retraining its deeper layers on our specific dataset. This allowed the model to adapt more closely to the nuances of our MRI images, enhancing its performance in distinguishing between different types of tumors and no tumor.

## Models Comparison
<div><b>Comparison of the Three Models</b></div>

<div>
  <img src='docs/model_comparison.png'>
</div>

## Data Source
https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

## License:
This project is licensed under the Raza Mehar License. See the LICENSE.md file for details.

## Contact:
For any questions or clarifications, please contact Raza Mehar at [raza.mehar@gmail.com], Pujan Thapa at [iampujan@outlook.com] or Syed Najam Mehdi at [najam.electrical.ned@gmail.com].
