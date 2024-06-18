---
title: 'Disease Detection from X-Ray Images with Classical Backbone Networks'
date: 2022-04-01
permalink: /projects/cxr_detection
image: "https://github.com/tarhanefe/tarhanefe.github.io/assets/73281981/e7b0ee8e-a33d-463a-be0e-b4b79c713190"
teaser: "https://github.com/tarhanefe/tarhanefe.github.io/assets/73281981/e7b0ee8e-a33d-463a-be0e-b4b79c713190"
---

This TUBITAK project aims to develop a system for detecting diseases from X-ray images using neural networks. The process involves preparing a dataset of X-ray images, where each image is labeled with various medical conditions. The images are preprocessed using OpenCV to resize them to 224x224 pixels, and the labels are binarized for multi-label classification. The project employs data augmentation techniques such as rotation, zoom, and shifts to enhance the training dataset. 


<p align="center">
<img src="https://github.com/tarhanefe/tarhanefe.github.io/assets/73281981/e7b0ee8e-a33d-463a-be0e-b4b79c713190" alt="Project Image" width = "400" /></p>



The core model used is VGG19, a convolutional neural network pre-trained on ImageNet, which serves as the backbone. This model is followed by a series of layers, including flattening and dropout, with a final dense layer that uses a softmax activation function to classify the images into multiple disease categories. The model is trained using the augmented data, with specific parameters for batch size and epochs, aiming to improve diagnostic accuracy and efficiency in detecting diseases from X-ray images.


[Link to the Github Repository](https://github.com/tarhanefe/DiseaseDetectionfromX-RayImageswithVisualTransformerNeuralNetworks-118C543-)

