# Melanoma Detection Assignment
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Libraries Used](#libraries-used)


## General Info
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion


## Conclusions
Model 1: The model's training accuracy shows a steady increase of upto 88%, while validation accuracy remains consistently around 53%. This clearly shows the presence of overfitting. To resolve this issue, augmentation techniques need to be employed. Since there is limited training data available, we need to generate new samples by making slight modifications to existing data (such as horizontal/vertical image flipping, minor image rotations, etc.), which will then be used for training the model.

Model 2: The issue of overfitting has been effectively addressed by leveraging augmented data, and both raining and validation accuracy of the above mentioned model fall within a similar range. But now the training and validation data are showing poor performance, indicating that the model is now exhibiting underfitting.

Model 3: After rectifing class imbalance, training and validation accuracy has enhanced dramatically. After using Batch Normalization, the model's training accuracy shows a steady increase of upto 97%, while validation accuracy remains around 82%. Even though the validation accuracy is good, there seems to be a bit of overfitting in this model. We will remove the batch normalization and try it out again.

Final Model: The final model showcases well-balanced performance, displaying no signs of underfitting or overfitting. The implementation of class rebalancing has notably enhanced the model's performance across both training and validation datasets. The training loss and validation loss are also not much different which is also a sign of good fit. The Validation accuracy is 0.82 which is good. The model is able to classify the images with 82% accuracy.

## Libraries Used
- Numpy
- Pandas
- Matplotlib
- Sklearn
- Tensorflow
- Augmentor
