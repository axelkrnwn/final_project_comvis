# NeuroScan
**⭐ Brain Tumor Detection Using Traditional Machine Learning**

A project for computer vision subject that predicts whether someone has brain tumor or not from brain image. This project aims to:

- Assist doctors in analyzing scans more quickly and accurately.
- Reduce the workload of medical professionals.
- Enhance overall efficiency in medical diagnostics.

## Contributors
1. Axel Kurniawan
2. Frederick Chandra
3. Hendra Hartanto

## Dataset
- the dataset were retrieved from the kaggle link below.

  [Dataset link here](https://www.kaggle.com/datasets/preetviradiya/brian-tumor-dataset)

## Explanatory Data Analysis (EDA)

1. This data contains 4600 Images with 2 labels. which is *brain tumor* and *healthy*. the brain tumor image has 2530 images and healthy has 2070.
2. The image color mode is dominated by RGB with percentage around 97%.
3. The size of the images is various from 256x256 to 1024x1024.
4. There is no missing value from the dataset.

## Preprocessing
  ### 1. Grayscale
  Grayscale process aims to standardize the dimensions across images.
  The dimesions needs to be standardized because the color feature in brain tumor detection in unneccesary. 
  ### 2. Resize
  Since the image size in the dataset is very various, resizing process can help to equalize the size of the image 
  ### 3. Median Blur
  Median blur aims to remove the noise from the image because in some images there is some random noise 
  The reason to choose median blur over other types of blur is because this type of blur robust to salt and pepper noise.

## Feature Extraction
  In this task, we use the texture feature over other types of features. the reasons why we use this type of feature are:
  - Texture feature can determine which part of brain is tumor.
  - The edge feature can be an alternative for this task too. but the edge feature can only be good when the tumor is located at the side of the image since it can make a huge difference between brain tumor and healthy.

  To maximize the feature extraction process, both local and global feature extraction technique were used in this task which are **LBP (Local Binary Pattern)** for local feature and **GLCM (Gray Level Covariance Matrix)** for global feature.

## Principal Component Analysis
  1. Principal Component Analysis is used to reduce dimensionality of dataset.
  2. This process aims to reduce dimensions in the dataset after feature extraction process.
  3. THis process reduces the dataset dimensions from 250 to 80 features.

## Splitting
  The dataset splitted into training and testing with ratio **7:3** using train_test_split

## Model Training
  - The model was trained using some machine learning algorithm such as logistic regression, SVM, decision tree, and random forest.
  - These algorithms were used because of its specialty in binary classification since this task aims to detect brain tumor or healthy.
  - After the training process, the best model was built using random forest with approximately 94-97% in every evaluation metric for test dataset.


