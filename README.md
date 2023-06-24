# Image Classification with CNN

In this project, I explore the various intricacies of the Tensorflow Framework to create an image classification model, 
classifying an image of a person as #Happy# or #Sad# based on their expressions.

#Source of data:

Google Images

##Problem Statement:

Create a create an image classification model that can train a convoluted neural network and perform classification on two types of human images - Happy and Sad
Labels: Happy(0) | Sad(1)

#Understanding of dataset:
 1. Since we downloaded the dataset from the web there were lots of corrupt files and files with invalid extensions
 2. The data cleaning part focused on removing such images from our data set to train an efficient model and mitigate any errors while training

#Creating a data pipeline:
1. Utilizing the image_dataset_from_directory utility function from Keras we created a data preprocessing pipeline
2. Lots of helper functions are associated with image_dataset_from_directory that help us transform and preprocess our data.
3. image_dataset_from_directory returns an array of batches with dependent and independent variables (batch size is configurable)
4. We then scale our data i.e. we scale down all the pixels in our images to a range of (0,1) from (0,255). This will allow our deep-learning model to learn faster
   since our optimizer function will be able to converge faster due to a lower range of values of variables.

#Deep Learning Model:
1. For the convolution operation layer we initialize 16 filters of size (3,3) and stride of 1
2. We then use the max pooling layer to extract the pixels with the largest values, indicating that these pixels highlight
   the most crucial features of our image.
