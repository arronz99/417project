# 417project

# Introduction
The purpose of this report is to demonstrate the materials and knowledge that reflect the curriculum of Machine Learning and Pattern Classification (ESE417 FL2021) at Washington University in St. Louis. The curriculum provides a mathematical and practical understanding of machine learning.

In order to demonstrate a thorough understanding of the material learned throughout the semester, this paper examines the performance of **support vector machines** and **random forest classifiers**; two classification methods that are covered in the class.
## Dataset Description
The dataset being utilized is the red wine quality data set from the University of California, Irvine (UCI) Machine Learning Repository. This dataset consists of 1599 samples of red wine north from Portugal. 

Each sample consists of the target feature, the quality of the wine, rated from 3 to 8, and eleven other features;
<ul>
  <li>Fixed Acidity</li>
  <li>Volatile Acidity</li>
  <li>Citric Acid</li>
  <li>Residual Sugar</li>
  <li>Chlorides</li>
  <li>Free Sulfur Dioxide</li>
  <li>Total Sulfur Dioxide</li>
  <li>Density</li>
  <li>pH</li>
  <li>Sulphates</li>
  <li>Alcohol</li>
</ul>

The UCI website states that the task of predicting the quality of the wine samples can be treated as either a regression or classification task. 

# Methods

## Support Vector Machine

### Overview of Algorithm
Support Vector Machine (SVM) is a classification algorithm that aims to construct a hyperplane to separate datapoints by their label. Although it is similar to perceptron classification, SVM is significantly stronger than perceptron classifiers. Since SVM maximizes the margin, or the distance between the hyperplane and the nearest points on either side, it is more robust when it comes to unseen testing data. Furthermore, SVM can address problems that are non-linearly seperable points by taking advantage of feature-space transformations. SVM comes in two flavors, hard margin or soft margin, to tackle seperable and non-seperable data, respectively. 

### Implementation of Algorithm
For our project, we used the scikit-learn implementation for SVC (C-Support Vector Classification). Here, there are three main hyperparameters: 
<ul>
  <li>C: Regularization parameter.
  They use an L2 penalty parameter, and C is inversely related to the strength of regularization. As such, C can be any positive real number. We specifically looked at a window of values between 0.05 and 1.5. 
  </li>
  <li>Kernel: feature-space transformations.
  There are several different candidate feature-space transformations in the universe of kernel functions. Specifically for the scikit-learn implementation, the main ones are linear, polynomial, RBF (Radial Basis Function), and sigmoid. Polynomial kernels require a degree for the transformation. The linear function is a specific instance of polynomial kernel (degree = 1).
  </li>
  <li>
  Degree.
  The degree is only used for a polynomial kernel and represents the polynomial degree transformation applied.
  </li>
</ul>


## Random Forest Classifier

There are three main hyperparameters for the random forest classifier:
<ul>
  <li>Fixed Acidity</li>
  <li>max depth. By the limiting the depth of individual decision trees, 'overfitting' on training data can be avoided. </li>
  <li>criterion. The criterion is the method by which the classifier decides which feature to make the decision feature for the root node of a tree. The two criterions available are entropy and gini.</li>
</ul>

# Comparison of Classification Methods
