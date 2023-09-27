# PCB-Components-Detection-using-Mask-RCNN using Tensorflow 2
This is an implementation of PCB (Printed Circuit Board) components detection  using Mask R-CNN,using python 3.8,Tensorflow 2.5.0.
Detecting components on a printed circuit board (PCB) is a critical task in electronics manufacturing and quality control. The accurate identification and localization of various components such as capacitors, integrated circuits, connectors, and more are essential for ensuring the functionality and reliability of electronic devices. One powerful approach to tackle this problem is using Mask R-CNN (Mask Region-based Convolutional Neural Network), a deep learning model that excels in object detection and segmentation tasks. This project has achieved a remarkable milestone by attaining an impressive Mean Average Precision (mAP) score of 0.91 for detecting critical components, including capacitors, integrated circuits (ICs), connectors, and transistors..

 ![jh](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/22914e99-462c-4756-ada4-66e235cd9a4e) 


Annotation tool used : VGG annotator (https://www.robots.ox.ac.uk/~vgg/software/via/) please download the zip file

Backdone used for feature extraction is ResNet101 which performed better than ResNet50 but the model is very complex for the training data which consists of 1971 images(total 20790 region of interest) and 717 validation images (13506 region of interest).Some of the techniques that are followed to improve the model :
1) **Learning Rate Schedular** - This help to schedule the learning rate after each epoch and aviods the vanishing or exploding gradient descent issue.
2) **Adam Optimizer** - Instead of using SGD Optimizer Adam optimizer is used as it can prevent overfititng of model
3) **Data Preprocessing** - Some techniques such as center cropping,converting into gray scale,flipping,rortation at different angles, image enhancement techniques (brightness,contrast and saturation) where applied before training model and then annotated to increase the size of dataset. finally this technique have improved my model from mAP of 0.45 to 0.91. (Without applying image augmentation during model training, training data and validation data is increased by 60%)
4) Hyperparamater Tunning - The given below table represents the hyperparameters of the model.

![HYP1](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/b49fe9e5-6bce-4020-8ac9-32fcc63abd19)
![HYP2](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/d1c68daf-9dfa-49ea-83ae-006e3ac98d3e)
![HYP3](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/ddd4b7bf-a58c-436d-ac75-f39ebd4a1799)

In this project, I have developed a Flask-based web application that leverages the capabilities of Mask R-CNN to automate the detection of PCB components. This application provides a user-friendly interface for users to upload images of PCBs, and it returns annotated images with components highlighted and labeled.

![ezgif com-video-to-gif](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/0657a0da-529b-4718-95d1-29efc4f408f4)

![f1_1](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/6e6f0e21-fc0a-4050-8588-1ceebe39fe08)
 ![f2](https://github.com/dayana123456789/PCB-Components-Detection-using-Mask-RCNN/assets/99783461/f75abc83-6e7a-4b61-b484-46deaac55b25)


