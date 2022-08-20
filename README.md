## Integrating-Remote-Sensing-and-Street-View-Imagery-to-Map-Slum
This repository is dedicated to my MSc. thesis, in which I have integrated Remote Sensing Imagery (RSI) and Street View Imagery (SVI) to map slums using a deep learning approach.
The research aims to map the slums in dense urban environments using FCN-DK deep learning architecture. In this research, we have integrated overhead information with ground-level information to understand the urban context of the study area (Jakarta), i.e., integrate the RSI and SVI.

We have selected Jakarta as our study area because around 60% of the Jakarta population lives in informal settlements called Kampungs.

## The repository includes:
VGG16-Place365 implementation includes:
1. Loading Dataset SVI and Labels
2. Visualization of Dataset and Labels
3. Setting the pre-trained VGG16-Places365
4. Retraining the model using SVI 
5. Evaluation of trained model on the testing data set
7. Generating accuracy metrix
8. Calculating accuracy assessment through Overall Accuracy, Precision, Recall, and F1 Score

Feature extraction from SVI
The 128 features were extracted from each SVI using retrained VGG16-places365 model just before the classification layer. Then 128 features were reduced to 32 features using Principal Component Analysis. Note: Then, using the spatial interpolation technique, 32 feature maps were generated using ArcGIS, all 32 layers were stacked, and one 32 band imagery was generated.

Modified FCNDK implementation includes:
1. Loading Dataset (RSI and SVI) and Labels
2. Visualization of Dataset and Labels
3. Generating patches for training the model
4. Building Modified FCNDK Network for taking three inputs, i.e., RSI, SVI, and Labels
5. Defining the Number of classes and Training Configuration
6. Training Model
7. Evaluation of the trained model by testing on testing data set
8. Generating accuracy metrix
9. Calculating accuracy assessment through Overall Accuracy, Precision, Recall, and F1 Score

## Data Set
For this Msc. research work data was aquired as follows:
1. WorldView 3 satellite imagery of 0.41 m spatial resolution was aquired through ESA Grand wich was granted by writting proposal to ESA.
2. Street view imagery was aquired using Google Street View Static API service
3. Reference data was aquired by Jakarta's local government official website
