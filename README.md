# FaceRecognition
Our goal here is to use Python with openCV to create an program capable to recognize faces from an dataset. This code are based in the presented in this post (https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/) on pyimagesearch

OpenCV incorporates some basic cascades which have very good practical applications such as Face Recognition. 

To do that we are going to obtain some dataset to train our data, it will be classified onto to categories:

* Positive Images: are images that contain our object and
* Negative Images: are images the doesn't contain our object

Our step by step will be

1. Applying face detection
2. Applying face alignment and cropping
3. Applying face recognition with our deep neural network

# **Prerequisites**

1. Python
2. OpenCV
3. Anaconda