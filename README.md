# Dog-Breed-Classification-

Project Overview:
Objective of the project is to build a deep learning model using convolution neural
networks to classify the given image to one of the dog breeds.

Problem Statement:
Given an input image, the algorithm will first detect if the input image is a dog image
and tell its breed.

Analysis:
Data Set
Datasets is downloaded from the below locations.
dog_images_url = https://s3-us-west-1.amazonaws.com/udacity-aind/dogproject/dogImages.zip.

Data Exploration:
Dog datasets is downloaded and unzipped to project folder.
Dog images are placed in 3 folders train, test and val.
Each of the folders further have 133 sub folders for each of the dog breeds.
Each of the 133 folders in turn have several dog images for training, validation and
testing.
Storing the data in this folder format enable the pytorch/keras to read the data with
folder name and classification labels.

Algorithms and Techniques:
There are multiple steps involved in achieving the results which will be discussed in
detail later in this document. We will be mainly using these algorithms.
1. Predict if the given image is an image of dog.
Here again we are using pre trained model and predict if the given image is an
image of a
dog, since we don’t have sufficient data to predict the image for dog vs non dog
image.
And also the VGG16 model is trained on large amount of crowd sourced dataset,
with works
with great accuracy for our problem in this step.
VGG16 have 1000 image classification. After the network predicting the index of the
classification and analyzing the classification value,we can see the index starting
from 151 to
268 corresponds to different dog breed classifications.
We use these values to predict if the image is an image of a dog or not.
2. Pytorch based CNN implementation from scratch to classify the dog images We
are using CNN neural network algorithm to solve the image classification problem
since this techniques are proven to work best with the image data. Several
convolution layers are stacked with number of kernels and nodes in each layer are
taken mostly with the trail and prior knowledge in the area.
Each of the CNN layers will learn different features of the image like lenes, edges,
curves,
color gradations etc, we can already see the model is trying to mimic the human
behaviour
like we also try to see different features of the image to understand what the image
is.
3. As a final step we combine all the above implementation in the simple python
function to make the required prediction.
