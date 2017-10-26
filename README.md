# Kaggle Competition | Porto Seguro’s Safe Driver Prediction
From the competition [homepage](https://www.kaggle.com/c/porto-seguro-safe-driver-prediction).

>In this competition, you’re challenged to build a model that predicts the probability that a driver will initiate an auto insurance claim in the next year. While Porto Seguro has used machine learning for the past 20 years, they’re looking to Kaggle’s machine learning community to explore new, more powerful methods. A more accurate prediction will allow them to further tailor their prices, and hopefully make auto insurance coverage more accessible to more drivers.

### Data Description

>In the train and test data, features that belong to similar groupings are tagged as such in the feature names (e.g., *ind*, *reg*, *car*, *calc*). In addition, feature names include the postfix *bin* to indicate binary features and *cat* to indicate categorical features. Features without these designations are either continuous or ordinal. Values of **-1** indicate that the feature was missing from the observation. The *target* columns signifies whether or not a claim was filed for that policy holder.

### Notebook Content
iPython Notebook [here](https://github.com/Jihenghuang/kaggle-porto-seguro/blob/master/porto-seguro-jiheng.ipynb)
* About Missing Data
* Drop Redundant Features & Replace Missing Data
* Data Preparation
* Feature Selection (Random Forest Classifier)
* Train A Model (Linear Regression)
* Predict & Output
* Kaggle Score

### Reference and Future Work
For the random forest classifier part in this project , I referenced codes from [Prof. Ravi Shroff](http://cusp.nyu.edu/people/ravi-shroff/) 's Machine Learning class at CUSP.

I think there are two ways to improve this project: 

First of all, when creating dummy variables for categorical features, my code used a lot of computing resources and create sparse matrix due to the **104** unique values feature *ps_car_11_cat* has. Although the random forest classifier reduced dimensionality later in the project, I am still searching for better ways to convert categorical features at this step. 

Secondly, try more prediction algorithms, obviously. I can add more models in the future working on this project.

### Analysis Highlights
* Missing Data

<p align="center">
  <img width="700" height="280" src="http://jihenghuang.com/wp-content/uploads/2017/10/5-Features-with-Most-Data-Missing.jpg">
</p>


* Correlation between features

<p align="center">
  <img width="1000" height="500" src="http://jihenghuang.com/wp-content/uploads/2017/10/Correlation-Between-Features.jpg">
</p>

* Remaining Feature Data Distribution
![alt text](http://jihenghuang.com/wp-content/uploads/2017/10/Feature-Data-Distribution.jpg)
* Use Random Forest Classifier, the top 20 features contributing to a claim to be filed (target = 1)

|       | feature_select | feature_importance|
|-------|:--------------:| -----------------:|
|1      |      ps_car_13 |           0.098262|
|2       |     ps_reg_03   |         0.093183|
|3|            ps_car_14    |        0.057226|
|4    |        ps_ind_03     |       0.051262|
|5     |       ps_ind_15      |      0.051083|
|6|            ps_reg_02       |     0.049227|
|7 |           ps_ind_01        |    0.036896|
|8  |          ps_car_15         |   0.036607|
|9   |         ps_reg_01          |  0.036353|
|10   |         ps_car_12          |  0.027303|
|11|           ps_car_11|            0.012646|
|12 | ps_car_01_cat_11.0 |           0.008632|
|13  | ps_car_09_cat_2.0  |          0.008630|
|14   |ps_ind_04_cat_0.0   |         0.008376|
|15 |  ps_ind_02_cat_1.0    |        0.008298|
|16  | ps_ind_04_cat_1.0     |       0.008273|
|17   |ps_ind_02_cat_2.0      |      0.008004|
|18 |      ps_ind_16_bin       |     0.008000|
|19  | ps_car_09_cat_0.0         |   0.007793|
|20  | ps_car_01_cat_7.0        |    0.007719|

* AUC score (produce probabilistic predictions) on training dataset

0.59645323858

* Accuracy score (predict the class)

0.963615286396

* Train A Model: Logistic Regression to Predict
Output sample

|	id|	target|
|--------------:| -----------------:|
|	0| 0.027729|
|	1	|0.032712|
|	2	|0.022809|
|	3|	0.020033|
|	4|	0.035388|
|	5	|0.030271|
|	6	|0.019810|
|	8	|0.019596|
|	10	|0.066153|
|	11	|0.043696|

* Submit to Kaggle Competition

Current normalized Gini score: 0.241

