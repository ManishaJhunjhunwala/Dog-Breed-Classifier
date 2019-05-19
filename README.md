# Dog-Breed-Classifier
In this project, I have build a pipeline to process real-world, user-supplied images. Given an image of a dog, my algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed. 

# 1st Part of the project
In the first part of the project, I have created a CNN that classifies dog breeds. The CNN is created from scratch. 
In the 2nd part of this notebook, I have used transfer learning to create a CNN that attains greatly improved accuracy.

The task of assigning breed to dogs from images is considered exceptionally challenging. To see why, consider that even a human would have trouble distinguishing between a Brittany and a Welsh Springer Spaniel.

# Creating a CNN to Classify Dog Breeds (using Transfer Learning)
I have used Densenet201 as my pretrained model to make a classifier to predict the dog breeds. Densenet201 is a very powerful architecture having 201 hidden layers. It works very well in case of image classification problems. I have compared 2 architectures - Resnet152 and Densenet201 but densenet worked better in terms of giving accuracy.

First I am freezing the entire model and just redefining the classifier part and training the model to achieve around 87% accuracy. To train the model further, we unfreeze the whole model and start training the entire model having changed weights and biases. This approach gives a very good accuracy and low validation loss.

Optimizer used is Adam and Loss is calculated using NLLLoss.

