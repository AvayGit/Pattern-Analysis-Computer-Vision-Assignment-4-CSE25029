# Pattern Analysis — Assignment 4

## Overview

This repository contains the implementation of **Assignment 4** for Pattern Analysis. The project applies different machine learning approaches to an image dataset, covering unsupervised, supervised, semi-supervised learning, dimensionality reduction, and a complete pattern-recognition pipeline.

## Objectives

The assignment implements:

1. K-Means Clustering
2. K-Medoids Clustering
3. Gaussian Mixture Model
4. Supervised and Unsupervised Learning
5. Bayesian Classification
6. K-Nearest Neighbour Classification
7. Artificial Neural Network Classification
8. Semi-Supervised Classification
9. Dimensionality Reduction
10. Complete Pattern-Recognition System

## Dataset

The project uses the supplied **Pattern Analysis Image Dataset**.

The expected dataset structure is:

```text
Pattern_Analysis_Image_Dataset/
├── Class_1/
│   ├── image1.png
│   ├── image2.png
│   └── ...
├── Class_2/
│   ├── image1.png
│   ├── image2.png
│   └── ...
└── Class_3/
    ├── image1.png
    ├── image2.png
    └── ...
```

The class names are obtained automatically from the dataset folder structure.

## Feature Extraction

The image-processing pipeline extracts a combination of:

* Histogram of Oriented Gradients (HOG)
* RGB color histograms
* Grayscale statistical features

The extracted features are standardized using `StandardScaler` before machine learning algorithms are applied.

## Machine Learning Methods

### K-Means

K-Means clustering groups the image features into the detected number of classes. The clusters and centroids are visualized using a two-dimensional PCA representation.

### K-Medoids

K-Medoids clustering is implemented on the same standardized image-feature dataset. The resulting clusters and medoids are visualized and compared with K-Means.

### Gaussian Mixture Model

A Gaussian Mixture Model is used to perform probabilistic clustering. The model produces cluster assignments as well as membership probabilities for individual samples.

### K-Nearest Neighbour

KNN classification is performed using multiple values of `K`. The test accuracy for each value is calculated, and the best-performing `K` is selected for the final model.

### Gaussian Naive Bayes

Gaussian Naive Bayes is trained using the extracted image features. Its performance is evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.

### Artificial Neural Network

A basic multilayer perceptron neural network is trained for image-class classification and evaluated using the held-out test dataset.

### Semi-Supervised Learning

Label Spreading is used to simulate a partially labelled dataset. Most training labels are hidden while a smaller portion remains labelled. Its performance is compared with supervised classification.

## Dimensionality Reduction

The project applies four dimensionality-reduction techniques:

* PCA
* LDA
* ICA
* t-SNE

Each technique produces a two-dimensional representation that is visualized according to the known image classes.

## Evaluation Metrics

The project uses:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Adjusted Rand Index (ARI)
* Normalized Mutual Information (NMI)

ARI and NMI are used primarily for evaluating unsupervised clustering against the known class labels.

## Complete Pattern Recognition Pipeline

The final section combines the major stages of the project:

```text
Image Dataset
      ↓
Feature Extraction
      ↓
Feature Standardization
      ↓
Dimensionality Reduction
      ↓
Train-Test Split
      ↓
Classification
      ↓
Confusion Matrix
      ↓
Accuracy / Precision / Recall / F1
      ↓
Model Comparison
```

KNN and Gaussian Naive Bayes are used as the primary classifiers in the complete pipeline.

## Google Colab

The implementation is designed to run in **Google Colab** with the dataset stored in Google Drive.

The dataset path used by the notebook is:

```text
MyDrive/Pattern_Analysis_Image_Dataset
```

The notebook automatically creates the output directory:

```text
MyDrive/CSE25029_Assignment_4_Output
```

## Output Files

The generated results are organized into separate folders:

```text
CSE25029_Assignment_4_Output/
├── KMeans/
├── KMedoids/
├── GMM/
├── Supervised_Unsupervised/
├── Bayesian/
├── KNN/
├── ANN/
├── Semi_Supervised/
├── Dimensionality_Reduction/
├── Complete_System/
├── FINAL_SUMMARY.csv
├── clustering_comparison.csv
└── overall_classification_comparison.png
```

The output directory contains visualizations, CSV result files, extracted feature arrays, trained models, classification reports, confusion matrices, and summary results.

## Requirements

The notebook uses Python and the following major libraries:

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Scikit-image
* Pillow
* Joblib

The required packages can be installed in Google Colab using:

```python
!pip -q install scikit-image scikit-learn pandas matplotlib seaborn joblib
```

## How to Run

1. Upload the `Pattern_Analysis_Image_Dataset` folder to Google Drive.
2. Open the notebook in Google Colab.
3. Run the cells sequentially from beginning to end.
4. Allow Google Colab to access Google Drive.
5. Wait for feature extraction and model training to finish.
6. Check the generated results inside `CSE25029_Assignment_4_Output`.

## Author

**CSE25029**

Pattern Analysis — Assignment 4
