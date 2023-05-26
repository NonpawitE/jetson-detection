# Garbage detection using Jetson Nano 
Garbage detection from the input picture 
# Preparing the Data 
Gather the dataset from https://www.kaggle.com/datasets/asdasdasasdas/garbage-classification . The dataset includes 6 different types of garbage including paper, plastic, trash, cardboard, glass and metal.
# Annotation and augmentation
•	Annotate and label tool: Cvat 

•	Export the data in Pascal VOC v 1.1 format (including the annotating) 

•	Augment the picture on Roboflow by uploading the images and annotations

•	Export the augmented dataset into YOLO v7 Pytorch format

•	Augmentation: flip, crop, and rotation 

•	Data Split: Training 80%, validation 20%, Test 0% 

•	Total images in dataset: 5.9k for training and 493 images for validation 

# Model Training 
•	YOLOv7 is used for training our customized data and the training is performed in Google Colaboratory.

•	There are 5 main parts including installing dependencies, downloading customized data, model training, evaluation, and prediction.

•	Install dependencies: Git clone yolov7 to Google Colab and install the requirements.txt

•	Download customized data: We can either upload the customized dataset by downloading the zip file from Roboflow or get the code from Roboflow and download the data on Google Colab.

•	Model training: Download the weights for training from YOLOv7. Then, begin the training by adjusting the batch size, number of epochs, and specific where our data.yaml file is located.

# Evaluation and Prediction 
•	Evaluation: When training is done, we can look at our model performance by confusion matrix, f1-score, precision, and recall graph which are in the train folder in yolov7 that we git clone from the beginning

•	Prediction: We used detect.py that provide in the YOLOv7 folder. Then locate the path of the weights that we got from the training, the image that want to detect, and we can adjust the confidence score as well.
