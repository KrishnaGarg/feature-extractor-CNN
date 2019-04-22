# Feature Extraction for Images Dataset #
[Source code credits: https://github.com/Gogul09/flower-recognition]

### Dependencies ###
* Theano or TensorFlow `sudo pip install theano` or `sudo pip install tensorflow`
* Keras `sudo pip install keras`
* NumPy `sudo pip install numpy`
* matplotlib `sudo pip install matplotlib` and you also need to do this `sudo apt-get install python-dev`
* seaborn `sudo pip install seaborn`
* h5py `sudo pip install h5py`
* scikit-learn `sudo pip install scikit-learn`

### Modifications ###

1.	Modify conf.json
See the existing file, replace visdial-sample with approprite dataset that you add [visdial-sample is the name I use for my dataset folder and for the folder where features are extracted]

2.	Directory structure changes required:
a.	dataset/visdial-sample/db1 folder
The appropriate place to copy your images for which you want to extract the images. I copied the images of train, test, val images one-by-one and extracted the features.

b.	output/visdial-sample/vgg16 folder
The empty folder to be created before you run go for extracting features.

### Usage ###
* Organize dataset                      - `python organize_flowers17.py`
* Feature extraction using CNN          - `python extract_features.py`
* Train model using Logistic Regression - `python train.py`
* Output - features.h5 [created in output/visdial-sample/vgg16 folder]