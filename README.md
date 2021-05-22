# Chest X-ray Pneumonia Classification

In this repository a classifier was trained to distinguish between chest x-ray with pneumonia and normal
## Dataset
The dataset from kaggle contained 3 directories : train, test and validation
I merged the 3 of them and resplit the data into train and test data as you can find in the notebook.

below is an example of chest x-ray diagnosed with pneumonia and one diagnosed as normal:

<p float="left">
  <img src="/dataset/NORMAL/IM-0001-0001.jpeg" width="200"  height="200" title="NORMAL" />
  <img src="/dataset/PNEUMONIA/person3_virus_17.jpeg" width="200" height="200" title="PNEUMONIA"/> 
</p>

## Training
To speed up the training, I used vgg16 pretrained model (as described in the original paper below)
![GitHub Logo](/assets/vgg_architecture.PNG)


## Result
The model could reach in only 10 epochs :
- Loss of 0.00976
- Accuracy of 0.988


#### References
VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION paper
Kaggle Dataset : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia/data
