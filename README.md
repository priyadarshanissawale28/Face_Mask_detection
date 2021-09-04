# Face_Mask_detection
Face_Mask_Detection
PART - 1
# Face mask detection using MobileNet:-
+ Traing the model:

## Dataset:-
+ It contain 7553 images, 3723 labelled as with_mask and 3828 labelled as without_mask.
** Sample images from dataset:-
+ It includes Both dataset (with face mask/Without face mask)
+https://www.kaggle.com/omkargurav/face-mask-dataset/download

## Training:-
+ Here We are Loading The MobileNetV2 model from keras and using its pretrained weights for base model.
 and we have added a few additional layers, following Dense layer at the end with softmax activation function.
## Results:-

we achived 97.08% accuracy on training data set. this can aggumented with our face detection model in order to get the face mask detection.

**output :- (on test video from youtube)
https://929687.smushcdn.com/2407837/wp-content/uploads/2020/04/face_mask_detector_plot.png?lossy=1&strip=1&webp=0
+** output :- ![Screenshot (110)](https://user-images.githubusercontent.com/88090830/132086182-1a4578d2-0c38-4362-8de3-92347bc91cef.png)


### Part :- 2

#### Face detection using HaarClassifier:
#### Face detection:
##### 1. Using DNN Face detector:
It is a Caffee model based on SSD (Single sot Multibox Detector) and ResNet-10 architecture. It is available in OpenCV.

1. Load network using *cv2.dnn.readNetFromCaffe* passing the weights and layers as arguments. The files for weights and layers are added in the repository (protxt and weights)
Caffe stores and communicates data using blobs.

2. *cv2.dnn.blobFromImage*: cv.dnn.blobFromImage(image[, scalefactor[, size[, mean[, swapRB[, crop[, ddepth]]]]]]) 
Creates 4-dimensional blob from image. Optionally resizes and crops image from center, subtract mean values, scales values by scalefactor, swap Blue and Red channels.
[OpenCV documentation]

This is passed to the network and faces are detected.


