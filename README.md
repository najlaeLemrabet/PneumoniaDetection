# Chest X-ray Pneumonia Classification

In this repository a classifier was trained to distinguish between chest x-ray with pneumonia and normal
## DATASET
The dataset from kaggle contained 3 directories : train, test and validation
I merged the 3 of them and resplit the data into train and test data as you can find in the notebook.

Below is an example of chest x-ray diagnosed with pneumonia and one diagnosed as normal:

<figure>
  <img src="/dataset/NORMAL/IM-0001-0001.jpeg" alt="my alt text"/>
  <figcaption>This is my caption text.</figcaption>
</figure>

<p float="left">
  <img src="/dataset/NORMAL/IM-0001-0001.jpeg" width="200"  height="200" title="NORMAL" />
    <img src="path_to_image" alt>
    <em>image_caption</em>
  <img src="/dataset/PNEUMONIA/person3_virus_17.jpeg" width="200" height="200" title="PNEUMONIA"/> 
</p>
Kaggle Dataset : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia/data

## TRAINING
To speed up the training, I used vgg16 pretrained model (as described in the original paper below), the vgg16 convolutional layers and a simple fully connected layers as classifier were used.

![GitHub Logo](/assets/vgg_architecture.PNG)

Hyperparameters:
- epochs = 10
- learning rate = 0.001
- bacth size = 10

Loss function and optimizer:
- Mean square error loss
- Adam optimizer

## Result
The model could reach in only 10 epochs :\
loss = 0.00976\
accuracy = 0.988


#### References
VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION paper
