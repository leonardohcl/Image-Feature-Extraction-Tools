
# Image Feature Extraction Tools
This repository holds python scripts that allow the extraction of different features form images using  a variety of techniques. Additionaly there's also a small library to make easier some of the steps of the proccess.

## Extended Library
This files holds some of the general functions used all over the scripts, they are:

- [FileHandling.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/FileHandling.py):  Functions to deal with files like creating a '.csv' file with the contents of a folder or creating a '.arff' file;

- [Dataset.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/Dataset.py): Holds the ImageDataset class that handles opening files, transforming them, associating image with class and other operations used with Convolutional Neural Networks (CNNs);

- [CNN.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/CNN.py): Functions to manage CNNs like training routines;

- [CAMHelpers.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/CAMHelpers.py): Functions that help generate images from extracted Class Activation Maps (CAMs).

## CNN Training
To extract deep features from a CNN, either with ou without any transfer learning, it may be necessary to apply some training to the network. At [training_exemple.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/training_example.py) you'll find a guide to apply this training to a network using the tools provided here and from external packages.

## Deep Features Extraction
The values from a CNN internal layer can hold relevant information describing the patterns on an Image. When these values are used as features, they're known as deep features. At  [layer_extraction_example.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/layer_extraction_example.py) there's a quick script showing how to obtain those and save it as a '.arff' file.

## CAM Extraction
A Class Activation Map shows which areas of an image contribute more to the final result. This information can be used in many forms, and can be obtained following the script at [cam_extraction_example.py](https://github.com/leonardohcl/Image-Feature-Extraction-Tools/blob/main/cam_extraction_example.py). The script shows how to acquire these CAMs in four different ways: a grayscale map, a colormap, a colormap overlaying the original image and multiply overlay of the grayscale map on the original image. Here are some examples of the resulting images obtained from a VGG16 CNN pre-trained on the Imagenet dataset:

**Original Image**

<img src="https://user-images.githubusercontent.com/33093068/141047550-ac30d8ef-1ad3-4862-8f4e-bed78a35fb09.jpg" alt="Original Imaga to be processed and generate the CAMs" width="400"/>

**Grayscale CAM**

<img src="https://user-images.githubusercontent.com/33093068/141047083-10de8d2f-7a56-4acf-8f9f-4e4b8643acb9.png" alt="Grayscale CAM generated" width="400"/>

**Colormap CAM**

<img src="https://user-images.githubusercontent.com/33093068/141047626-f3bfd149-ac20-417a-b569-de16576c808b.png" alt="Colormap CAM generated" width="400"/>

**Colormap overlay CAM**

<img src="https://user-images.githubusercontent.com/33093068/141047660-6f33f822-166d-48e8-b7d8-97da5964453a.png" alt="Colormap overlay CAM generated" width="400"/>

**Grayscale multiply CAM**

<img src="https://user-images.githubusercontent.com/33093068/141047743-bf25d92e-a536-4792-931f-772d8471c374.png" alt="Grayscale with a multiply overlay CAM generated" width="400"/>

## Packages

These scripts use some external packages that are listed below with the versions installed on the development environment.

[PyTorch](https://pytorch.org/) v1.10

[Pillow](https://pillow.readthedocs.io/en/stable/) v8.2

[Numpy](https://numpy.org/) v1.20.2

[pandas](https://pandas.pydata.org/) v1.2.4

[Matplotlib](https://matplotlib.org/) v3.4.3

[pytorch-grad-cam](https://github.com/jacobgil/pytorch-grad-cam) v1.3.1
