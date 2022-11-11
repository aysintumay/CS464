# CS464
Homeworks and Project of CS465-Introduction to Machine Learning course in Bilkent University, Fall 2022.
Python 3 is used on Juypter Notebook. 

The BBC Sports News dataset is used.  The goal is to predict the class  of the sports news in the validation set. The class labels (the last column) are from 0 to  4.  There are 4613 words. Training data has 552 documents while test data has 185 documents. The train and validation sets are uploaded on the Jupyter notebook files of the related directory.  

This is a Bag-of-Words implementation with Multinomial Naive Bayes Classifier. 2 classifiers are built to train the data and test on the validation set. None of the machine learning libraries is utilized.  Only NumPy, Pandas, Matplotlib and Math packages are used to perform efficient computation. 

At the beginning, an Explatory Data Analysis is done on the train and validation sets to discover some statistical properties.

The likelihoods and priors are generated. After ; MLE(), classify(), evaluate_classification() functions are generated. The computations follow from calling these methods for both estimators. 
MLE function computes 2.6 depicted in the manual giving -inf= np.nana_to_num(-np.inf). It takes the likelihoods as input and outputs a 185x5 matrix containing the ML estimations of each class for each document in validation set.
classify() function classifies each document by comparing the probabilities of each class. In case of ties, class 0 (athletics) is chosen. It takes the output of MLE as input and outputs the confusion matrix.
evaluate_classification() takes the confusion matrix as input and it outputs the accuracy and the number of wrong predictions. It compares if the ground truth is equal to the prediction.

In the first half of the implementation, MLE is used by generating the priors, and likelihoods. In the second half, MLE is extended to generate a MAP estimator with the smoothing factor of alpha=1. 
The accuracies, confusion matrices and the number of wrong predictions are reported below each method.

