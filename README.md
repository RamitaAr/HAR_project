# Welcome to a deep learning project implementation for Human activity recognition (HAR) using data from smartphones 
The project aims at developing deep learning model (convolutional neural network) to effectively learn accelerometry dataset collected using smartphones for human activity prediction purposes. This work opens up an opportunity to be used in wearables devices and to track daily activity for patients with mobility issues such as people with Parkinson's disease, ALS and PAH. 

The Main code in this repository is modified from a tutorial and use public datasets to train and test the model's performance.

A link to tutorial page: https://towardsdatascience.com/human-activity-recognition-har-tutorial-with-keras-and-core-ml-part-1-8c05e365dfa0

# Download Datasets
To be able to run the code, you will need to download these datasets. 
Link to datasets:
1. https://www.cis.fordham.edu/wisdm/dataset.php
2. https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones

# Data Pre-processing
After downloading the datasets, they will need to be combined by combining WISDM with UCI (only laying data) to achieve a complete 7 basic activity labels in daily life(Sitting, Standing, Walking, Laying, Upstairs, Downstairs) to train the model.

First, since UCI raw accelerometry dataset and its activity labels come in separate files, it needs to be pre-processed by adding the activity labels into the dataset. Followed by down sampling the dataset from 50 Hz to 20 Hz for the sampling rate to be matched with WISDM dataset.

This can be done by running the following file: UCI_pre-processing.ipynb in ‘Data pre-processing’ folder.

Next, run the following file ‘data remodel (WISDM + UCI).ipynb’  to extract only laying data from UCI and combine with  WISDM dataset. 

# Main Code - Data cleaning, train and test the CNN model
Lastly, run the main code “CNN_allact_updated.ipynb” to train and test the model's performance. Note that all the data cleaning and normalizing process are in the main code.

# Data Augmentation
Apply data augmentation technique to improve model's performance. 