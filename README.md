# Chest X-ray Pneumonia Classification

In this repository a classifier was trained to distinguish between chest x-ray with pneumonia and normal\
The repository includes:
- x-ray chest images Dataset
- jupyter notebook containing all the steps: data loding ,data preprocessing, training, testinh
- Pre-trained weights

## DATASET
The dataset from kaggle contained 3 directories : train, test and validation
I merged the 3 of them and resplit the data into train and test data as you can find in the notebook.

Below is an example of chest x-ray diagnosed with pneumonia and one diagnosed as normal:

<p float="left">
  <img src="/dataset/NORMAL/IM-0001-0001.jpeg" width="200"  height="200" title="NORMAL" />
  <img src="/dataset/PNEUMONIA/person3_virus_17.jpeg" width="200" height="200" title="PNEUMONIA"/> 
</p>
Kaggle Dataset : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia/data

## TRAINING
I used vgg16 pretrained model (as described in the original paper below) to speed up the training, the vgg16 convolutional layers (backbone) and a simple fully connected layers as classifier.

![GitHub Logo](/assets/vgg_architecture.PNG)

Hyperparameters:
- epochs = 10
- learning rate = 0.001
- bacth size = 10

Loss function and optimizer:
- Mean square error loss
- Adam optimizer

## RESULTS
![GitHub Logo](/assets/accuracy.PNG)


The model could reach in only 60 epochs :\
training accuracy = 0.0.9869
testing accuracy = 1.0

#### REFERENCES
VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION paper
