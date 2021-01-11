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



# Directory tree

C:.
│   extract_embeddings.py
│   README.md
│
├───dataset
│   ├───ChrisPratt
│   │       cp1.jpg
│   │       cp10.jpg
│   │       cp2.jpg
│   │       cp3.jpg
│   │       cp4.jpg
│   │       cp5.jpg
│   │       cp6.jpg
│   │       cp7.jpg
│   │       cp8.jpg
│   │       cp9.jpg
│   │
│   ├───DwayneJohnson
│   │       dj1.jpg
│   │       dj10.jpg
│   │       dj2.jpg
│   │       dj3.jpg
│   │       dj4.jpg
│   │       dj5.jpg
│   │       dj6.jpg
│   │       dj7.jpg
│   │       dj8.jpg
│   │       dj9.jpg
│   │
│   ├───SamiraHaddad
│   │       sh1.JPG
│   │       sh2.jpg
│   │       sh3.jpeg
│   │       sh4.jpeg
│   │       sh5.jpg
│   │
│   ├───ScarlettJohansson
│   │       sj1.jpg
│   │       sj10.jpg
│   │       sj2.jpg
│   │       sj3.jpg
│   │       sj4.jpg
│   │       sj5.jpg
│   │       sj6.jpg
│   │       sj7.jpg
│   │       sj8.jpg
│   │       sj9.jpg
│   │
│   └───ZoeSaldana
│           zs1.jpg
│           zs2.jpg
│           zs3.jpg
│           zs4.jpg
│           zs5.jpg
│           zs6.jpg
│           zs7.jpg
│
├───face_detection_model
│       deploy.prototxt
│       res10_300x300_ssd_iter_140000.caffemodel
│
├───images
│       GinaRodriguez.jpg
│       JameelaJamil.jpg
│       MichaelBJordan.jpg
│       RobertDowneyJr.jpg
│       SophieTurner.jpg
│       ViolaDavis.jpg
│
└───output

# **Prerequisites**

1. Python
2. OpenCV

## How to setup your environment ##

1. Install [Imutils](https://pypi.org/project/imutils/)

   $ pip install imutils

2. Install OpenCV Python

   $ pip install opencv-python

3. Install scikit-learn

   pip install -U scikit-learn



## Extract embeddings

To execute extract_embeddings.py do it:

$ python extract_embeddings.py --dataset dataset \

​	--embeddings output/embeddings.pickle \

​	--detector face_detection_model \

​	--embedding-model openface_nn4.small2.v1.t7

## Train face recognition model



$ python train_model.py --embeddings output/embeddings.pickle \

​	--recognizer output/recognizer.pickle \

​	--le output/le.pickle

[INFO] loading face embeddings...

[INFO] encoding labels...

[INFO] training model...

$ ls output/

embeddings.pickle	le.pickle		recognizer.pickle