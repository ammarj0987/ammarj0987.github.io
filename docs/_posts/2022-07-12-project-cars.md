---
layout: post
title: "Car Classification"
---

([Github Link](https://github.com/ammarj0987/Computer-Vision))

<p>I implemented and tested multiple training models on stanford's car dataset to compare the accuracy of each model. The dataset contains 8,144 training images and 8,041 testing images of a diverse group of cars. There are 196 labels in the form of Make, Model, Year of a car. For more information on the dataset: https://ai.stanford.edu/~jkrause/cars/car_dataset.html</p>

<p>Pytorch and torchvision are used to load classes from data and train on. Numpy and scipy are used to extract data from .mat file and load it into a py dictionary.</p>

<p>The images are of different sizes so to make use of tensors, I resized all images to 3 x 256 x 256. Because car designs and colors are very similar to each other, taking small random crops from the image was not as accurate. Images are also horizontally flipped 50% of the time in training. For parameters, I set the batch size to 32 and num_workers to 2. This is one batch of the data:</p>

![download](https://user-images.githubusercontent.com/105107071/173168942-d41992f3-b15b-4ed6-8c95-55a939ab81c7.png)

<p>The first model I used is called SimpleNet. It takes the flatten image size as inputs and output is set to 196. input is connected to hidden neurons by a fully connected layer and then hidden is connected to outputs in the same way. I then used a convolutional neural network which contains three convolutional layers and then uses a fully connected layer. I also tried another model called DarkNet which contains 3x3 convolutional layers with maxpooling ending with a global average pooling and fully connected layer. The last mdoel I used is resnet which I loaded from pytorch and reinitialized the final layer with 196 outputs.</p>

<p>For my training function, I used the following parameter values: epochs=10, lr=0.01, momentum=0.9, decay=0.0, verbose=1. For simpleNet, I set epochs to 5 because the loss remained the same after 5 epochs. After training each model, I got the folowing graph for losses:</p>

<p>Red - SimpleNet</p>
<p>Black - DarkNet</p>
<p>Blue - CNN</p>
<p>Green - Resnet</p>

![download](https://user-images.githubusercontent.com/105107071/173172740-b8f130cd-05b0-445a-b731-6094b11f59c8.png)

<p>After testing the models on training and testing data, I got the following results for accuracy:</p>

![Accuracy](https://user-images.githubusercontent.com/105107071/173174067-61091b17-2244-432b-9448-4d13ce8c3075.png)

<p>Since Resnet got the best accuracy, lets test it on some images</p>

![download](https://user-images.githubusercontent.com/105107071/173174140-968a8f62-6d56-45a3-8142-281cf9c35dd3.png)

<p>GroundTruth: Suzuki Aerio Sedan 2007 Ferrari 458 Italia Convertible 2012 Jeep Patriot SUV 2012 Toyota Camry Sedan 2012</p>

<p>Predicted: Suzuki Aerio Sedan 2007 Ferrari 458 Italia Convertible 2012 Jeep Patriot SUV 2012 Toyota Camry Sedan 2012</p>