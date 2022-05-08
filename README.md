# Final Project for CS 598: Deep Learning for Healthcare
For my final project, I attempted to reproduce the results of the paper "Mortality prediction of septic patients in the emergency department based on machine learning" by Perng et al. (available at https://pubmed.ncbi.nlm.nih.gov/31703390/) and the paper "Predicting 30-days mortality for MIMIC-II patients with sepsis-3: a machine learning approach using XGBoost" by Hou et al. (available at https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-020-02620-5). I was not able to find GitHub Repositories for either of these papers, but the paper by Hou et al. can be accessed through the link given, and is the data I used for this project.

In this project, the goal is to predict mortality in sepsis patients using features such as demographics, vital signs, and lab tests.

# Code
The code for this project, including preprocessing, training, and evaluation, is divided between the notebooks included in this repository. These notebooks are:

1 - Reproduce_Sepsis_Paper. This includes data preprocessing, and training and evaluation for the models logistic regression, support vector machines, random forest, gradient boosting, and k-nearest neighbors.

2 - Reproduce_Sepsis_Paper_PCA. This includes data preprocessing, using principal component analysis for dimensionality reduction, and training and evaluation for the models logistic regression, support vector machines, random forest, gradient boosting, and k-nearest neighbors.

3 - Reproduce_Sepsis_Paper_AE. This includes data preprocessing, training and using an autoencoder for dimensionality reduction, and training and evaluation for the models logistic regression, support vector machines, random forest, gradient boosting, and k-nearest neighbors.

4 - Reproduce_Sepsis_Paper_CNN. This includes data preprocessing, and training and evaluating a convolutional neural network.

These notebooks run in Google Colaboratory. To load the data, one can download the data from https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-020-02620-5, then upload it to their Google Drive and mount the drive to access the data from each notebook.

# Results

The results of evaluating these models are included below.

Performance of models with no additional feature construction or dimensionality reduction:

<img width="231" alt="Screen Shot 2022-05-08 at 6 02 15 PM" src="https://user-images.githubusercontent.com/33353757/167319447-30821ba9-b250-459b-8c60-61c323e10bee.png">

Performance of models with dimensionality reduction using PCA:

<img width="231" alt="Screen Shot 2022-05-08 at 6 03 07 PM" src="https://user-images.githubusercontent.com/33353757/167319463-8a568d4a-d6f3-4288-9983-b3787b5627c6.png">

Performance of models with dimensionality reduction using an autoencoder:

<img width="231" alt="Screen Shot 2022-05-08 at 6 03 17 PM" src="https://user-images.githubusercontent.com/33353757/167319467-b602cbf4-906b-45c1-831d-4b6940a66218.png">

Finally, the convolutional neural network had the worst performance with only 80.5% accuracy, and classified all patients as surviving.

From these results, I have reproduced the results of Hou et al. claiming the superior performance of a gradient boosting classifier. I have been unable to reproduce the results of Perng et al. claiming the superior performance of a CNN.
