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

### Analysis Highlights
* Missing Data
![alt text](http://jihenghuang.com/wp-content/uploads/2017/10/5-Features-with-Most-Data-Missing-in-Training-Dataset.jpg)

* Correlation between features
![alt text](http://jihenghuang.com/wp-content/uploads/2017/10/Correlation-Between-Features.jpg)

* Remaining Feature Data Distribution
![alt text](http://jihenghuang.com/wp-content/uploads/2017/10/Feature-Data-Distribution.jpg)

* Selected 20 most important features contributing to a claim to be filed (target = 1)
        feature_select  feature_importance
0            ps_car_13            0.098262
1            ps_reg_03            0.093183
2            ps_car_14            0.057226
3            ps_ind_03            0.051262
4            ps_ind_15            0.051083
5            ps_reg_02            0.049227
6            ps_ind_01            0.036896
7            ps_car_15            0.036607
8            ps_reg_01            0.036353
9            ps_car_12            0.027303
10           ps_car_11            0.012646
11  ps_car_01_cat_11.0            0.008632
12   ps_car_09_cat_2.0            0.008630
13   ps_ind_04_cat_0.0            0.008376
14   ps_ind_02_cat_1.0            0.008298
15   ps_ind_04_cat_1.0            0.008273
16   ps_ind_02_cat_2.0            0.008004
17       ps_ind_16_bin            0.008000
18   ps_car_09_cat_0.0            0.007793
19   ps_car_01_cat_7.0            0.007719
