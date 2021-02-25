# multilabel-classification-on--research-articles
This is a project about multilabel classification, there are 6 labels for every sample to predict. 
Test accuracy(6 labels) and Average accuracy(1 labes or more) are used for evaluation.

Multilabel classification probelem can be processed with following techniques:
## Problem transformation
* Binary relevance

  It is intuitively that the multi-label problem is converted into several binary classification problems.
  Each label is trained independently and each of the binary classifiers contribute separately to get the final result. 
  
* Label Powerset

  Label powerset method is the most natural approach, which generates a new label for every combination of labels in 
  training data and then solves the problem using multiclass classification approaches. 
  
* Classifier Chains

  Classifier Chains combine the computational efficiency of the Binary Relevance method while still being able to take the 
  label dependencies into account for classification. This is quite similar to Binary Relevance, the only difference being 
  it forms chains in order to preserve label correlation. 

KNN, Logistic Regression, Multinomial NaiveBayes, SVM , Ensemble Learning and ect. are used in each method.

## Adapted algorithms
* MLKNN
 
* MLARAM

These models have been adapted to the multi-label task, without requiring problem transformations.
## Neural network

Multi-label classification can be supported directly by neural network models by specifying the number of target labels 
as the number of nodes in the output layer. Each node in the output layer use the sigmoid activation. This will predict
a probability of class membership for the label, a value between 0 and 1. And the neural network model is fit with the
binary cross-entropy loss function. 

Becides, there are also have imbalance issue, we use SMOTE, here is the reference:
https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/
