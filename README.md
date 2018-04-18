# White Blood Cell (WBC) data analysis
Projects (mostly deeplearning) related to the white blood cell [dataset](https://github.com/dhruvp/wbc-classification/tree/master/images) from [Athelas](https://athelas.com/).

## Data
The **train data** consists of 10,000 images divided into four balanced WBC classes. The images were originally drawn from 352 dyed WBC images and are the result of the following pre-processing steps:

- downsample the images from 640x480 to 160x120
- image augmentation (flips, rotations, and shears)
- balancing the large class imbalance so that there are 2500 of each WBC type
- normalize (divide by 255) the images so the intensities are in the (0,1) range

You can read more about the data pre-processing [here](https://blog.athelas.com/classifying-white-blood-cells-with-convolutional-neural-networks-2ca6da239331).   

The **test data** consists of 71 images (20% of the original 352 images was set aside). The images have not been augmented; the original distribution has also been preserved so this is an imbalanced dataset.


## [Transfer Learning Project](https://github.com/Meena-Mani/wbc/blob/master/wbc_transferlearning_binary.ipynb)
Transfer Learning is widely used in deep learning to leverage models trained on very large data sets. For image classification tasks, models pretrained with ImageNet are usually used. In radiology and  pathology projects where the equivalent of ImageNet is not available, the interesting question is how would transfer learning models pretrained with ImageNet perform.

Here we look at a very small dataset which consists of stained images of four types of white blood cells (WBC): Eosinophils, Neutrophils, Lymphocytes or Monocytes. We are interested in seeing if we can successfully classify them as polynuclear or mononuclear with transfer learning using an InceptionV3 model pretrained on ImageNet.

