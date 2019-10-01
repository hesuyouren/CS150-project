## Overview

All our code is stored in one jupyter notebook file: "data_mining.ipynb". Just excute every block of code in order and you should be able to get promising results.  

Also we have run all the code block in "data_exploration.ipynb" to get a better feeling for this dataset.  
At the end of "data_exploration", you will see an additional code block which we used for testing whether "test.csv" file has been exported correctly and the result is good.  

----------

### Dependencies:

numpy==1.16.4  
pandas==0.24.2  
matplotlib==3.1.0  
scikit-learn==0.21.2  
pyspark==2.4.3  

(Note: this version of pyspark must run in a specific version of java, see info below)  
(run in terminal)  
$ java -version  
openjdk version "1.8.0_212"  
OpenJDK Runtime Environment (build 1.8.0_212-8u212-b03-0ubuntu1.18.04.1-b03)  
OpenJDK 64-Bit Server VM (build 25.212-b03, mixed mode)  


### Functions:

#### preprocessing:
this function is designed to extract student id, unit, section, problem name, step, view, kc, opportunity count from the entire dataset.

#### postprocessing:
this function is designed to assemble sid, unit, section, problem name, step and their CFARs, along with view, opportunity count and vectorized kc, into a single 203 dimentional feature vector.

#### rmse:
used to evaluate the rooted mean squared error

#### acc:
used to evaluate the accuracy of a classifier


### Variables:

#### uniqueFeatures:
A Dictionary which stores the corresponding "Correct First Attempt Ratio" of each feature: sid, unit, section, problem name and step.

#### lgtr:
Logistic Regression Model

#### lr:
Linear Regression Model

#### mlpr:
Multilayer Preceptron Regressor

#### knc & knr:
K-NearestNeighbor Classifier & Regressor

#### dtr:
Decision Tree Regressor

#### rfc & rfr:
Random Forest Classifier & Regressor