# part-2-cnn-computer-vision
Computer Vision Problem Formulation and CNN Prototype

# Data source
https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

# Approach

The objective of this project is to build a CNN-based computer vision model capable of classifying images into four categories - 
1 dent
2 scratch
3 normal
4 stain

The overall approach involved - 
1. analyzing the dataset structure,
2. preprocessing the image data,
3. building a CNN model,
4. training the model on labeled images,
5. evaluating prediction performance using various metrics.

A Convolutional Neural Network (CNN) was selected because CNNs are highly effective for image classification tasks due to their ability to automatically learn visual patterns such as edges, textures, and defect shapes from images.

# Steps Performed

## 1. Dataset Analysis
The dataset consisted of four image classes - dent, scratch, normal and stain and image folders for each class and an Excel file containing image IDs and labels.
The dataset was analyzed to determine - 
1 total number of classes
2 number of images per class
3 image dimensions
4 dataset balance
Sample images from each class were visualized to understand visual differences between defect categories.

# 2. Image Preprocessing
Before training the CNN model, images were preprocessed using Python.
The preprocessing included -
1 resizing all images to a fixed size (128×128)
2 converting images into numerical arrays
3 normalizing pixel values between 0 and 1
4 splitting the dataset into training and testing sets
5 applying image augmentation techniques

Image augmentation techniques included -
1 rotation
2 zooming
3 shifting
4 horizontal flipping
This helped increase data diversity and reduce overfitting.

# 3. CNN Model Development
A CNN model is built using TensorFlow/Keras.The architecture included - 
1 convolution layers
2 ReLU activation functions
3 max pooling layers
4 flatten layer
5 dense layers
6 dropout layer
7 softmax output layer
The convolution layers extracted image features, while pooling reduced image dimensions and preserved important patterns.
The output layer predicted probabilities for the four defect classes.

# 4. Model Training
The model is trained using the training dataset over multiple epochs. During training -
1 training accuracy
2 validation accuracy
3 training loss
4 validation loss
were monitored to evaluate learning performance.
Accuracy and loss curves were plotted to analyze model behavior.

# 5. Model Evaluation
The trained model was evaluated on unseen test images. Evaluation techniques included testing accuracy, confusion matrix, classification report, sample predictions.The confusion matrix helped identify correct and incorrect classifications across all classes. Sample predictions visually compared actual labels, predicted labels and confidence scores.

# Results

The CNN model successfully learned image features and achieved good classification performance on the test dataset.
Key outcomes -
1 high training accuracy
2 strong validation accuracy
3 decreasing loss values over epochs
4 successful prediction of image defect classes
The confusion matrix showed that most predictions were correctly classified along the diagonal.

The model demonstrated the ability to distinguish between - dents, scratches, stains and normal surfaces with good confidence.

# Observations

# 1. CNN Effectiveness
CNN layers effectively extracted visual features from images without manual feature engineering. The model automatically learned texture differences, edge patterns, surface defects etc. from training data.

# 2. Importance of Preprocessing
Image resizing and normalization significantly improved model training stability and convergence. Image augmentation improved generalization and reduced overfitting.

# 3. Balanced Dataset Advantage
Since all classes contained similar numbers of images, the dataset was balanced, helping the model learn all categories equally. This reduced prediction bias toward any specific class.

# 4. Model Limitations
Some confusion may still occur between visually similar defect classes such as -
1 dent vs scratch
2 stain vs normal
Increasing dataset size and training epochs could further improve accuracy.

# 5. Real-World Applicability
The developed CNN model can be applied in real-world industrial quality inspection systems for automated defect detection and product quality monitoring.

# Final Conclusion

The project successfully demonstrated how CNNs can be used for image classification tasks involving defect detection. By combining image preprocessing, convolutional feature extraction, pooling operations, and deep learning classification layers, the model learned to classify images into dent, scratch, normal, and stain categories effectively. The project highlights the practical application of computer vision and deep learning in automated inspection and industrial quality control systems.
