# Using Deep Learning to Identify Dog Breeds
*This project is the Capstone Project of the Udacity's [Data Scientist Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025).*

## Overview
There are hundred of different dog breeds in the world, some of which are very similar, thus for someone who is not an expert it can be difficult to differentiate them or to simply know what breed a certain dog is.

The goal of this work is to train a model that is capable of estimating the breed of a dog, given a certain image. Moreover, if provided with an image of a human, the model should be able to detect it and say to which type of dog the human looks like.

For image classification tasks, using Convolutional Neural Networks (CNN) is often the best choice as they work great for finding patterns in complicated images. In this project will see how to build a CNN from scratch and how to use "Transfer Learning" to take advantage of pre-trained models to achieve better performance.

This project was done using Python 3.9.12 and the libraries listed on the requirements.txt file.

A walkthrough of this project is available on [Medium](https://medium.com/@pcmaldonado/how-to-use-deep-learning-to-identify-dog-breeds-c4266adb4f15)

# Setup
To go through this project yourself, first you should download the the following files:

1. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 

2. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 

3. Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset.  Place it in the repo, at location `path/to/dog-project/bottleneck_features`.

Then you should be able to follow the different steps covered in the jupyter notebook, available on this repository:
- Detect Humans
- Detect Dogs
- Create a CNN to classify dog breeds (from scratch)
- Use a CNN to Classify Dog Breeds (using Transfer Learning)
- Create a CNN to Classify Dog Breeds (using Transfer Learning)
- Write the Algorithm to classify dogs
- Test the Algortihm


# Summary of the results
The first CNN built from scratch obtained 6.34% accuracy. However, by using transfer learning, i.e. using pre-trained models, we were able to get a much higher performance.

Three models were tested, each one with the same model architecture but trained on a different pre-trained model. The results are the following:

|             | Accuracy |
| ------------| ---------|
| VGG19       | 74.04    |
| InceptionV3 | 78.23    |
| Xception    | 85.4     |

Using the best performing model, Xception, with an accuracy of 85.4%, I was able to write an algorithm to classify the dogs and match the humans with their dog look-alikes:

![](https://cdn-images-1.medium.com/max/800/1*mwqWmp3TglOb-rRst6RsQA.png)
![](https://cdn-images-1.medium.com/max/800/1*SEIdDHBdBnr2zbK-QbuVBw.png)



# Acknowledgments
I would like to express my gratitude to Udacity for proposing such an interesting project, in addition to providing all the necessary materials to complete it.