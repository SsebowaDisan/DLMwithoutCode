
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

### DLTGUI Version 1.0.6

* Bug fixes.

### DLTGUI Version 1.0.5

* Now you can do data augmentation using Augmentor. 

### DLTGUI Version 1.0.4

* Now you can choose CPU or GPU before the training.
* You are able to choose activation function for singe-class training. (Sigmoid and ReLu [new])
* Added SimpleCNNModel
* Fixed bugs


### DLTGUI Version 1.0.2

* Fixed single class problem, now you can train one-class model,
* Added sigmoid as activation function and binary_crossentropy as loss function,
* Added new function to DLGUI (prepare_data, sigmoid and more)
* Added new example dataset.


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

### Dataset Folder Structure
The following is an example of how a dataset should be structured. Before you train a deep learning model, put all your dataset into datasets directory.

```
├──datasets/
    ├──example_dataset/
        ├── cat
        │   ├── img_1.jpg/png
        │   └── img_2.jpg/png
    ├──flower_photos/
        ├── daisy
        │── dandelion
        │── roses
        │── sunflowers
        │── tulips
        
For image classification.
```

# Usage

### Page - Home

1. Clone this repo.
2. ```cd Deep-Learning-Training-GUI```
3. On your conda terminal: ```pip install -r requirements.txt```
4. Set your dataset directory as I show above.
5. When you set your dataset, go to the terminal and run ```python app.py```. You can access the program on ```localhost:5000``` 
6. Now you will see the home page.


7. You must enter the path where your dataset is located. For example, I want to select the ```flower_photos``` folder in the datasets and I will write to the form element like this: ```datasets/flower_photos```
8. Split the dataset, we need to specify what percentage of the training data we will use as a test.
9. Pre-trained Models - Currently only MobileNetV2 is available, but in future versions you can easily select other pre-trained models for fine-tuning [not available yet].
10. CPU / GPU - You need to specify whether you want to train on the GPU or CPU (the first version will automatically run on the GPU).
11. Number Of Classes -  I'll go again from the flower_photos example. There are 5 separate folders under the ```flower_photos``` folder. This is our class count. When you train your own data set, you have to create as many folders here as you have classes.
12. Batch Size - Specifies whether the training samples are uploaded to the training network in escapes. If you have a 1080 Ti or better GPU, you can set it to 64 or 128. The higher Batch Size, less noise that the model learns.
13. Epoch - The number of training data shown to the model network. So if you make 10 Epoch, the training data will be shown to the model network 10 times.
 

# To-Do List

- [x] Release 5 pre-trained models.
- [x] Choosing CPU or GPU before the training.
- [x] Choosing Activation Function for singe-class training. (Sigmoid and ReLu)
- [x] Data Augmentation
- [x] Fine-Tuning
- [x] Heatmap on predicted images.
- [ ] Object Detection - Mask RCNN. 

# References 📚

- [Google - TensorFlow Datasets](https://www.tensorflow.org/datasets/catalog/overview) [1]

- [Google - TensorFlow Models](https://www.tensorflow.org/api_docs/python/tf/keras/applications) [2]

- [Google - TensorFlow  Transfer Learning](https://www.tensorflow.org/tutorials/images/transfer_learning) [3]

- [Font Awesome](https://fontawesome.com/) [4]

- [Boostrap V4](https://getbootstrap.com/docs/4.4/getting-started/introduction/) [5]

- [How to Easily Deploy Machine Learning Models Using Flask](https://towardsdatascience.com/how-to-easily-deploy-machine-learning-models-using-flask-b95af8fe34d4) [6]

- [Graphing Pretty Charts With Python Flask and Chartjs](https://blog.ruanbekker.com/blog/2017/12/14/graphing-pretty-charts-with-python-flask-and-chartjs/) [7]

- [Simple and efficient data augmentations using the Tensorfow tf.Data and Dataset API](https://www.wouterbulten.nl/blog/tech/data-augmentation-using-tensorflow-data-dataset/) [8]

- Marcus D Bloice, Peter M Roth, Andreas Holzinger, Biomedical image augmentation using Augmentor, Bioinformatics, https://doi.org/10.1093/bioinformatics/btz259 [9]


# DLMwithoutCode
