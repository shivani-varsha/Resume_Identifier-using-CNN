Resume Identifier using CNN model in Tensorflow Framework:

Overview:
This project aims to develop a resume classifier using only the visual characteristics of an image.
The goal is to accurately classify whether a given image is a resume or not, without relying on OCR or textual features.

Project Components:

1.Dataset Collection:
I have collected dataset of resume images and non-resume images and labelled them respectively.

2.Image Preprocessing:
Images are resized to a particular size (64,64) for uniformity.
Standard data preprocessing like normalization (rescale) is done.
Data Augmentation methods (featurewise_center, feature_std_normalization, horizontal_flip)
* featurewise_center is used to subtract the mean value of entire dataset or a specific feature from each data point.
* feature_std_normalization involves dividing each pixel value by the standard deviation of its channel.

3. Model Architecture:
I have chosen a CNN ( Convolutional Neural Network) for image classification with a total of 13 layers.
CNN Architecture:
1. 5 Successive Conv2D layer with 16, 32, 64, 128, 256 filters and kernel size of (3,3) followed by 5 MaxPool2D layer with a pool size of (2,2) and strides of (2,2).
2. To convert 3D output to 1D, Flatten layer is used.
3. 2 Fully connected dense layers (512, 256) units and with ReLU activation(function for non-linearity).
4. Final Output layer with 1 unit and sigmoid activation (as it is a binary classification).

4. Model Training:
The dataset is split into training and testing sets.
Adam optimizer is used and binary_crossentropy is used as loss function (to calculate the difference between true binary labels and the predicted probabilities).

5. Testing and Evaluation:
The model was evaluated on the testing set to assess its accuracy.
Results:
The model achieved a test accuracy of 70 % on the evaluation set.

Future Improvements:
To enhance the model's robustness, different architecture, adjustment of hyper parameters and with larger dataset can be done.
Accuracy might improve when NLP is additionally also added with it.
