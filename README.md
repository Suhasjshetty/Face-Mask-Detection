# Face-Mask-Detection

1.Detection using coloured mask dataset.

Libraries to install - cv2, os, numpy ,np_utils from keras.utils , load_model from keras.model.

Dataset - 

Steps for implementation:

Step 1) Importing the required libraries.

Step 2) Adding datasets to the data path . Datasets contains images of with mask and without mask. Creating empty list of data and target, after looping through the categories,         images are stored in data and images of with and without mask are appended to target.

Step 3) Converting the images into grayscale and resizing them.

Step 4) Sometimes images may not be available and face some error then it is handled by exception.
        Normalize the image by dividing it by 255 which converts pixel range into 0 and 1.
       Reshape the images into 4D because neural network takes 4D input.

Step 5) Building CNN model(Conv2D, max pooling, flatten and  dense layer(categorical)).

Step 6) Spliting the dataset into train and test set. I have trained for   epochs with test_size and  validation_split.

Step 7) We have made use of ModelCheckpoint to save the best epoch.

Step 8) For face detection we have used haarcascade_frontalface_alt.xml file.

step 9) Using VideoCapture(0) for webcam.
        Detecting the face.
        Converting into grayscale.
        Normalize the image by dividing it by 255 which converts pixel range into 0 and 1.
        Reshape the images into 4D because neural network takes 4D input.
        Creating a bounding box around the face and detecting whether the person is wearing a mask or no mask.

step 10) In cv2. imshow we use colored frames captured from the webcam.

By using dataset containing only white mask, so it will be able to detect if we are wearning a colored mask. 

