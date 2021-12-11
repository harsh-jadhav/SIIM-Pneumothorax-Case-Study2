# SIIM-ACR Pneumothorax Segmentation
![header image](https://miro.medium.com/max/700/1*IHzf11afYwRieoJbJgBH-g.jpeg)
- [Overview](#overview)
- [Dataset](#dataset)
- [Data Description](#data-description)
- [Project Goal](#project-goal)
- [Architectures used](#architectures-used)
- [Libraries used](#libraries-used)
- [Platform used](#platform-used)
- [Results](#results)
- [Directory Tree Structure](#directory-tree-structure)
- [Blog](#blog)
- [Web Application Demo Video](#web-application-demo-video)

## Overview:
Pneumothorax is basically a combination of two words Pneumo(air) and Thorax(chest). Pneumothorax is also known as lung collapse. Pneumothorax is caused by abnormal collection of air between the parietal and visceral pleura i. e. pleural space between lungs and chest wall. Pneumothorax is a relatively common respiratory disease that can occur in a wide range of patients and in various clinical settings.

Diagnosing a pneumothorax in a chest radiography image is not difficult for an experienced physician or radiologist, but in some cases, it can easily be missed. Usually it is diagnosed by a radiologist on a chest x-ray, and can sometimes be very difficult to confirm as discussed above. An accurate AI algorithm to detect pneumothorax would be useful in a lot of clinical scenarios. AI could be used to triage chest radiographs for priority interpretation, or to provide a more confident diagnosis for non-radiologists. In other words, a machine learning-based pneumothorax diagnosis technique from the chest X-ray image is required to assist a physician to diagnose a pneumothorax.

## Dataset:
This problem belong to one of the competitions held on kaggle, which can be found on following link:

https://www.kaggle.com/c/siim-acr-pneumothorax-segmentation/

The data is comprised of images in DICOM format and annotations in the form of image IDs and run-length-encoded (RLE) masks. Some of the images contain instances of pneumothorax (collapsed lung), which are indicated by encoded binary masks in the annotations. Some training images have multiple annotations.

![Sample Filled Mask](https://miro.medium.com/max/700/1*A9EYEB6O2mE3IKxib3sUBA.png)

images without pneumothorax have a mask value of -1.
![Sample Empty Mask](https://miro.medium.com/max/700/1*0rFVcuAqVxVL_bvPPyA8BA.png)

## Project Goal:

We have a dataset in the form of images, and our task is to predict the mask of pneumothorax in the X-ray image. This problem is of Semantic Image Segmentation problem. This model will assist a physician to diagnose a Pneumothorax.


## Architectures used:
### U-Net: https://arxiv.org/abs/1505.04597
![U-Net](https://miro.medium.com/max/700/1*lvXoKMHoPJMKpKK7keZMEA.png)

### Double-UNet: https://arxiv.org/pdf/2006.04868.pdf
![Double-UNet](https://miro.medium.com/max/700/1*iVi5typWa2Q2rv92oI9mQQ.png)

## Libraries used: 
Tensorflow, Keras, Flask

## Platform used:
Google Collab

## Results:
Model Weights: https://drive.google.com/file/d/1-1AmPmdIg-lb11-pVpxx0Hl9IxqVDVdB/view?usp=sharing
![Segmented Images](https://miro.medium.com/max/2400/1*3iGzllBiluoOAjlXaoKEhw.png)

## Directory Tree Structure:
```
├── Deployable Code
      ├── templates
      ├── uploads
      ├── .md
      ├── Flask_Deployment.ipynb
      ├── inference.py
      ├── model.py
      ├── sample_iusage.ipynb
      ├── utils.py
├── 2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.ipynb
├── 2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.pdf
├── Final_pipeline_Pneumothorax.ipynb
└── Final_pipeline_Pneumothorax.pdf
└── README.md
└── Weighted_Metrics_2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.ipynb
└── Weighted_Metrics_2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.pdf
└── harshjadhav100_Model_PneumoThorax.ipynb
└── harshjadhav100_Model_PneumoThorax.pdf
```

- Deployable Code: This folder contains all the files and code to deploy the model using Flask on Google Collab.
- harshjadhav100_Model_PneumoThorax.ipynb: This contains EDA and Vanilla Unet Implementation.
- 2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.ipynb: It contains Double Unet Implementation.
- Weighted_Metrics_2Block_DU_first_channel_harshjadhav100_New_Model_PneumoThorax.ipynb: It contains weighted metric that is used to measure the model performance.
- Final_pipeline_Pneumothorax.ipynb: It contains the simple pipeline for inference.

## Blog:
An article about this project: 
-->https://harshjadhav100.medium.com/siim-acr-pneumothorax-segmentation-d92af3086b51<--

## Web Application Demo Video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/XY9s1Kopuvs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

https://youtu.be/XY9s1Kopuvs
