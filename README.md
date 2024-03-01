# Deep Learning for Image and Video Processing Sign Language Letters and Digits Recognition

Neural networks are models who are trying to approximate a function given a specific set of data. The function’s space dimensions are determined by the number of features which describe a training example in the given dataset that was used to train the model. Any task that is given to a neural network can be divided in two broad categories, namely classification and regression tasks. In a classification task, the model will predict a certain value among others for a given set of values called classes, while in regression problems the predicted value can be any number and thereof is continuous. Convolutional neural networks are a type of artificial neural networks that are used in computer vision for image pattern recognition and feature extraction. Such models can be used in a classification setting to predict in which category an image belongs, for example whether the image depicts a dog or a cat. Since the introduction of such models, several architectures have been proposed with some of them yielding incredibly high accuracy scores such as the U-net for image segmentation and the mobilenetv2.

# Motivation

Deep learning neural networks fall under the category of machine learning algorithms and can be used for classification and regression tasks. In this project our focus is shifted more to convolutional neural networks that are used for classifying images and to the implementation of more sophisticate architectures such as mobilenetV2. The classification task is about sign language digits and letters recognition and different datasets were used for training all the created models. Furthermore, data augmentation techniques were used to introduce more diversity to our datasets and improve the performance of the models. Most of the models were training in a local machine but for models with larger complexity cloud GPU computing was used. After training each model, several metrics were obtained that gave us a better insight of those models’ performance.

# Data preprocessing and data augmentation

As mentioned earlier the models created were trained on a set of sign language letters and digits images. Different combinations of datasets were used to create the training dataset and all the images used were obtained from the Kaggle website. The three figures below depict some of the images for each dataset used.

![Figure 2](fig2.png)

# Methods

Initially, a model with a relatively small number of parameters was used for the execution of the classification task (36 classes in total). The network is composed of a rescaling layer which is responsible for setting each pixel value of the inserted image between 0 and 1. Following that, 5 convolutional and max pooling layers are used for reducing the size of the image and perform feature extraction. As the network goes deeper the number of filters for each convolutional layer is increasing. Particularly, the first convolutional layer has 16 filters, and that number is doubled for each next layer with the last one having 256 filters as depicted in Figure 1 below.

![Figure 1](fig1.png)

# Transfer Learning

Transfer learning is a machine learning method that was first introduced in the early 1980s. Given a large-scale machine learning model that has been trained on a huge amount of data e.g., VGG16, the idea is that this model maybe can be reused to different classification tasks. Thus, it is believed that the model after its training, has acquired a general like knowledge and can perform similar tasks by training only the top part of the model. The layers which do not take part in the training process are called frozen layers since their parameters do not get updated. Several combinations of frozen and unfrozen layers can be used to test which one gives the best performance.

![Figure 3](fig3.png)