# Predictive Analysis Using Breast Cancer Wisconsin (Diagnostic) Data set

Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image.
n the 3-dimensional space is that described in: [K. P. Bennett and O. L. Mangasarian: "Robust Linear Programming Discrimination of Two Linearly Inseparable Sets", Optimization Methods and Software 1, 1992, 23-34].

This database is also available through the UW CS ftp server:
ftp ftp.cs.wisc.edu
cd math-prog/cpo-dataset/machine-learn/WDBC/

Also can be found on UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29

Attribute Information:

1) ID number
2) Diagnosis (M = malignant, B = benign)
3-32)

Ten real-valued features are computed for each cell nucleus:

a) radius (mean of distances from center to points on the perimeter)
b) texture (standard deviation of gray-scale values)
c) perimeter
d) area
e) smoothness (local variation in radius lengths)
f) compactness (perimeter^2 / area - 1.0)
g) concavity (severity of concave portions of the contour)
h) concave points (number of concave portions of the contour)
i) symmetry
j) fractal dimension ("coastline approximation" - 1)

The mean, standard error and "worst" or largest (mean of the three
largest values) of these features were computed for each image,
resulting in 30 features. For instance, field 3 is Mean Radius, field
13 is Radius SE, field 23 is Worst Radius.

All feature values are recoded with four significant digits.

Missing attribute values: none

Class distribution: 357 benign, 212 malignant

Data set link: https://www.kaggle.com/uciml/breast-cancer-wisconsin-data

# Conclusion

In this self-guided project of mine I have tired to build a predictive model to predict whether a breast cancer tumor sample is malignant or benign by using different properties of it, such as radius, texture, perimeter etc. First we dropped all the unnecessary columns(i.e: 'id' and 'unnamed: 32'). Then we create to dataframes names 'dataM' which contained all the samples with malignant tumors and 'dataB' which contained all the samples with benign tumor. With the help of these two dataframes we plot the histogram for all the features and analised the corelation between various features with our target label. After visualizing the data we importer pycaret library to build our machine learning models. We compared all the models and 'Extra Trees Classifier' model yielded us the highest accuracy (96.73%) We then tuned the model and the number of false negatives was only two (1.1%).
I also tried to  build a univariate model with only 'radius_mean' as the feature and the accuracy was not high as the multi-variate model(87.67%) also the number of false negatives are high.

This project helped me to visualize corelation between different features of the breast cancer tumor and build a predictive analysis model with 96.73 % accuracy and only 1.1% false-negatives. The project has further room for improvement and I will keep improving the model as I keep learning various machine learning techniques. Also the project is uploaded to my github repository, feel free to contribute.

#### Avishek Chatterjee
#### Jadavpur University
#### Department of Mechanical Engineering
#### 15-07-2020
