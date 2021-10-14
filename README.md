
# Description
My goal is to simplify the installation and training of pre-trained deep learning models through the GUI (or you can call web app) without writing extra code. Set your  dataset and start the training right away and monitor it with TensorBoard or DLTGUI tool. No more many parameters, no more data preprocessing.

While developing this application, I was inspired by the DIGITS system developed by NVIDIA.


* You won't have any problems for training image classification algorithms.
* It is easy to train a image classification model, save the model, and make predictions from the saved model.
* A few parameters!
* You will be able to train on pre-trained models.
* It doesn't exist for 1.0 but,  it will be much easier to train  and use object detection algortihms.
* You can train your model on GPU or CPU.
* Parallel operation is possible.
* You won't be needing a second terminal and a script code to run TensorBoard.

In the words of Stephen Hawking:
> Science is beautiful when it makes simple explanations of phenomena or connections between different observations. Examples include the double helix in biology and the fundamental equations of physics.



# Updates

### DLTGUI Version 1.0.9
- Bug Fixes (There was a problem about showing heatmap  for Cuda >= 10.0, fixed). 

### DLTGUI Version 1.0.8

* Bug fixes.

### DLTGUI Version 1.0.7

* Many bugs have been solved.

* You will be able to Fine-Tuning your model. In this way, you can easily increase the success rate of the model. 

* You will be able to see which parts your model focuses on while classifying images (Class activation map, heat map - heatmap - available for MobileNetV2 only)


### DLTGUI Version 1.0.1:
* Now you can use InceptionV3, VGG16, VGG19 and NASNetMobile models. [Image Classification]

# Getting started
### Prerequisites
- Anaconda 64-bit
- Python 3.7.3
- Tensorflow 2.0.1 
- CUDA and CUDNN ( Minimum Cuda 10.0 - for gpu usage)
- Numpy 1.16.4
- Matplotlib
- PIL
- subprocess
- pathlib
- Augmentor


# Available models
* MobileNetV2
* Inception V3
* VGG16 
* VGG19
* NASNetMobile
* SimpleCnnModel

# DLMwithoutCode
