Dermatology Disease Classification

This repository contains a comprehensive analysis of a dermatology dataset using multiple machine learning techniques, including Gradient Descent, Random Forest, k-Nearest Neighbors, KMeans Clustering, and Agglomerative Clustering. The objective is to classify dermatological diseases based on clinical and histopathological attributes and visualize the results.

Introduction

The goal of this project is to analyze and classify dermatological diseases based on various clinical and histopathological attributes collected during a study in a dermatology department. We utilize several machine learning methods to classify diseases and visualize the results to identify patterns and insights.

Dataset

The dataset used for this analysis contains the following attributes:

Clinical Attributes (values 0, 1, 2, 3 unless otherwise indicated):

Erythema
Scaling
Definite borders
Itching
Koebner phenomenon
Polygonal papules
Follicular papules
Oral mucosal involvement
Knee and elbow involvement
Scalp involvement
Family history (0 or 1)
Age

Histopathological Attributes (values 0, 1, 2, 3):

Melanin incontinence
Eosinophils in the infiltrate
PNL infiltrate
Fibrosis of the papillary dermis
Exocytosis
Acanthosis
Hyperkeratosis
Parakeratosis
Clubbing of the rete ridges
Elongation of the rete ridges
Thinning of the suprapapillary epidermis
Spongiform pustule
Munro microabscess
Focal hypergranulosis
Disappearance of the granular layer
Vacuolization and damage of basal layer
Spongiosis
Saw-tooth appearance of retes
Follicular horn plug
Perifollicular parakeratosis
Inflammatory mononuclear infiltrate
Band-like infiltrate

The dataset contains 34 attributes, with the 35th being the class label, i.e., the disease name. The names and ID numbers of the patients were removed from the database.

Installation

To run the analysis, you need to have Python installed along with the following libraries:

numpy
pandas
matplotlib
seaborn
scikit-learn
statsmodels

Analysis and Results

Part 1: Gradient Descent - Classifying Disease by Patient Age

Using the gradient descent algorithm to classify diseases based on patient age resulted in low accuracy due to the complexity of the dataset.

Gradient Descent Accuracy: 31%


Part 2: Random Forest on Clinical and Histopathological Features

A random forest classifier was fit to all features in the dataset, achieving high accuracy through multiple iterations.

Mean Random Forest Accuracy (50 Iterations): 94.57%


Part 3: k-Nearest Neighbors on Clinical and Histopathological Features

Initial KNN models did not perform well, but accuracy improved significantly after applying Sequential Feature Selection.

Initial KNN Model Accuracy (100 Iterations): 69.22%

Final KNN Model Accuracy (100 Iterations): 97.84% (with 22 selected features)

Part 4: KMeans and Agglomerative Clustering on Clinical and Histopathological Patient Data

Both clustering methods were used to classify patient data, showing the abilities of unsupervised learning.

KMeans Model Accuracy: 81.01%
Agglomerative Model Accuracy: 86.31%

Overall Results

The analysis highlights the varying performance of different machine learning methods on a dermatology dataset. Gradient Descent showed limitations with low accuracy, while Random Forest and KNN demonstrated high accuracy when using a diverse set of features. Clustering methods provided insights into the underlying structure of the data, with Agglomerative Clustering performing slightly better than KMeans.

License:
This project is licensed under the MIT License.
