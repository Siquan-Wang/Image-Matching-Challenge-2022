# Image Matching Challenge 2022

The process to reconstruct 3D objects and buildings from images is called Structure-from-Motion (SfM). Typically, these images are captured by skilled operators under controlled conditions, ensuring homogeneous, high-quality data. It is much more difficult to build 3D models from assorted images, given a wide variety of viewpoints, lighting and weather conditions, occlusions from people and vehicles, and even user-applied filters.

The first part of the problem is to identify which parts of two images capture the same physical points of a scene, such as the corners of a window. This is typically achieved with local features (key locations in an image that can be reliably identified across different views). Local features contain short description vectors that capture the appearance around the point of interest. By comparing these descriptors, likely correspondences can be established between the pixel coordinates of image locations across two or more images. This “image registration” makes it possible to recover the 3D location of the point by triangulation.

Google employs Structure-from-Motion techniques across many Google Maps services, such as the 3D models created from StreetView and aerial imagery. In order to accelerate research into this topic, and better leverage the volume of data already publicly available, Google presents this competition in collaboration with the University of British Columbia and Czech Technical University.

The task is to create a machine learning algorithm that registers two images from different viewpoints. With access to a dataset of thousands of images to train and test your model, top-scoring notebooks will do so with the most accuracy.
## Description

•	Developed adaptions of detector-free local feature matching with transformers (LoFTR) and deep kernelized dense geometric matching (DKM) to extract local features and register two images from different viewpoints with 0.82 mean average accuracy

•	Used test time augmentation (TTA) with size transformations and flips at the LoFTR inference stage in Python to avoid overfitting

•	Filtered and merged the coordinate pair array results of LoFTR and DKM, and calculated the fundamental matrix with  OpenCV new RANSACs to facilitate the structure-from-motion (SfM) techniques to map the 3D world with unstructured image collections 


## Getting Started

### Dependencies

* Kaggle Notebook

## Authors
Siquan Wang

sw3442@cumc.columbia.edu

## License

N/A

## Acknowledgments

competition website:
* https://www.kaggle.com/competitions/image-matching-challenge-2022
