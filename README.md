# Cancer-diagnosis
the model classifies weather the cancer is Malignant or Benign.

### LIBRARIES
* numpy
* pandas
* seaborn
* matplotlib
* sklearn

### DATA SET
* This dataset contains around 570 Cancer diagnosis examples .
* There are 32 features in total for the dataset including the target column weather the cancer is Malignant or Benign.
* The dataset can be downloaded from the zip file in this repository

### CLEANING DATA
there are no null value in the data set to fill

### FEATURE ANALYSIS
There are too many features so to prevent from overfitting more dependent features are dropped. By plotting the heatmap it is clear that many features are correlated , the features that are more correlated
are found out using scatter plot and dropped.

-> The features perimeter_mean, area_mean ,perimeter_worst, area_worst are heighly corelated with radius_mean and radius_worst,
concavity_mean, concave points_mean, fractal_dimension_mean, concavity_se,concave points_se, fractal_dimension_se are heighly corelated with compactness_mean and compactness_se,
concavity_worst, concave points_worst ,perimeter_se, are heighly corelated with compactness_worst and radius_se,

So the features perimeter_mean, area_mean ,perimeter_worst, area_worst, concavity_mean, concave points_mean, fractal_dimension_mean,
concavity_se,concave points_se, fractal_dimension_se, concavity_worst, concave points_worst ,perimeter_se are DROPPED.

### SPLITTING DATA
As they are around 570 the data set was splitted into 80% train 20% test sets.

### TRANING
This data is trained on several models :  
* XGBoost
* SVM
* RandomForest
* k nearest neighbour 
* Logistic regression

### EVALUATION METRIC 
As they are almost equal number of examples for both the classses accuracy is the single evalution metric.
* model with highest accuracy

### MODEL COMPARISON

| MODEL        | Class 1 RECALL(malignant) |      Class 0 RECALL(benign)       | ACCURACY |
| -------------|:-------------------------:|:---------------------------------:| --------:|
| XGBoost      |         0.96              |             0.93                  | 94.73%   |
| SVM          |         0.93              |             0.98                  | 94.73%   |
| RandomForest |         0.96              |             0.93                  | 94.73%   |
| k nearest neighbour |  1.00              |             0.89                  | 95.61%   |
| Logistic regression |  0.96              |             0.93                  | 94.73%   |


### BEST MODEL 
# KNeighborsClassifier with ACCURACY 95.61%

