# Detection of COVID-19 From X-ray images Using Deep Convolutional Neural Network(CNN).

## Introduction:
 
Coronavirus disease 2019 (COVID-19) is an infectious disease caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2).The disease was first identified in December 2019 in Wuhan, the capital of China's Hubei province, and has since spread globally, resulting in the ongoing 2019–20 coronavirus pandemic.About 3 million people have been suffering from this pandemic .Among several ways for detection, I tried two approaches using X-ray and CT-scan. I suppose using them  is a faster, easier and less harmful method than others.Lungs of those patients(infected from Covid) were  presented with patchy ground glass opacities(GGO),crazy paving appearances and air space consolidation.

This is a standard Convolutional neural network model for detecting covid-19 from X-ray.

## Datasets:

 Datasets are collected from several sources. Two categories of data were collected for training and testing:x-ray and CT-Scan. X-ray non covid(normal and pneumonia) data are extracted through kaggle whereas X-ray covid-19 datasets are extracted from the github open source. CT-Scan datasets ,both covid as well non covid were fetched from github open source.
  
   Non-covid image        |      covid image
:-------------------------:|:-------------------------:
![](https://github.com/Aliza211/COVID-19-Detector/blob/master/data/non_covid_xray/14.jpeg) |  ![](https://github.com/Aliza211/COVID-19-Detector/blob/master/data/covid_xray/5_preprocessed.png)


         
## Data augmentation:

 Due to less number of covid-19 positive images, images were augmentated by using the operations of horizontal and vertical flipping and rotation.

## Approach:

 Several standard models like VGG16,ResNet50,InceptionV3 have been implemented for transfer learning.Among them, VGG-16 gave the best result. Due to some limitation of data (Noise and small) different methods have to be followed.  

At first, X-ray data was trained in a standard pretrained model by freezing some layers.Almost 99% percent training accuracy and 98% of validation accuracy was achieved.After that CT-scan datas are also trained on the pretrained model of x rays.

## Result:

   Confusion matrix as well precesson table is shown below.


![](https://github.com/Aliza211/COVID-19-Detector/blob/master/images/Screenshot%20from%202020-04-29%2020-47-28.png)
 
 
![](https://github.com/Aliza211/COVID-19-Detector/blob/master/images/Screenshot%20from%202020-04-29%2020-47-54.png)


model can be downloaded from:
https://drive.google.com/open?id=1VBgyJiurgMJCYz7AhCVhalZnP5XijulQ

## Further work:
The model for CT-scan is still to be improved.The models can be further improved after availability of more covid-19 positive x-ray and CT-scans images.

