# Project 2 Ames House Price Prediciton Model

### Obejctive:  
#### 1. Create a model that have a high probability of predicting correctly the house value based on features with high coefficient.
#### 2. List down 3 most important features that have a great effect on the value of a house.


### Steps:

1. EDA
2. Data Cleaning
3. Feature Selection & Engineering
4. Modelling & Evaluation
5. Conclusion & Summary

------------------------------------------

## 1. EDA

After loading the data set I check for null values for both train and test data. Then I plot a histogram for the target value to find out whether it is normally distributed.

### Plot histogram for SalePrice to find out if it has normal distribution
![saleprice_hist](https://github.com/Mr-Ahmad-Khalil/Predicting-House-Price-Ames-Dataset-/blob/main/Images/saleprice_hist.png)

#### Features with more than 0.5 correlation to SalePrice: 

|Feature|Correlation|
|--------|-------|
|SalePrice|1.000000|
|Overall Qual|0.800207|
|Gr Liv Area|0.697038|
|Garage Area|0.650270|
|Garage Cars|0.648220|
|Total Bsmt SF|0.628925|
|1st Flr SF|0.618486|
|Year Built|0.571849|
|Year Remod/Add|0.550370|
|Full Bath|0.537969|
|Garage Yr Blt|0.533922|
|Mas Vnr Area|0.512230|
|TotRms AbvGrd|0.504014|


### From the highly correlated features plot graphs to find outliers and remove them

![grlivarea_vs_saleprice](https://github.com/Mr-Ahmad-Khalil/Predicting-House-Price-Ames-Dataset-/blob/main/Images/grlivarea_vs_saleprice.png)
![overallqual_vs_saleprice](https://github.com/Mr-Ahmad-Khalil/Predicting-House-Price-Ames-Dataset-/blob/main/Images/overallqual_vs_saleprice.png)

### The two outliers each has a Saleprice of 160000 and 183850 respectively

### EDA Summary:

#### For the train dataset:
1. The distribution for the saleprice is not normal

2. The top 5 correlated features to saleprice are:
- Overall Qual = 0.800207
- Gr Liv Area = 0.697038
- Garage Area = 0.650270
- Garage Cars = 0.648220
- Total Bsmt SF = 0.628925
 
3. Columns with high amount of missing values:
- Lot Frontage = 330
- Garage Yr Blt = 114
- Mas Vnr Type = 22
- Mas Vnr Area = 22

4. The two outliers have Saleprice of 160000 and 183850.    
    
#### For the test dataset:
1. Columns with high amount of missing values:
- Lot Frontage = 160 
- Garage Yr Blt = 45



## 2. Data Cleaning

1. Replace values from the column 'MS SubClass' to their string values not int.
2. Replace Ordinal values with numerical
3. Replace Continuos values with null values to 0
4. Replace Nominal values with null values to NA
5. Impute missing data from 'Lot Frontage' using KNN
6. Drop irrelevant columns that has more than 50% missing values:
  - Pool QC =          99.56%
  - Misc Feature =    96.83%
  - Alley  =           93.17%
  - Fence =          80.50%
  - Fireplace Qu = 48.76%


#### Dummify the categorical (nominal) columns:
1. MS SubClass
2. MS Zoning
3. Street
4. Land Contour
5. Utilities
6. Lot Config
7. Neighborhood
8. Condition 1
9. Condition 2
10. Bldg Type
11. House Style
12. Roof Style
13. Roof Matl
14. Mas Vnr Type
15. Foundation
16. Heating
17. Central Air
18. Sale Type
19. Garage Type
20. Exterior 1st
21. Exterior 2nd
22. Mas Vnr Area
23. Bsmt Full Bath
24. Bsmt Half Bath
25. BsmtFin SF 2
26. Garage Area
27. BsmtFin SF 1
28. Garage Cars
29. Bsmt Unf SF
30. Total Bsmt SF

## 3. Feature Selection & Engineering

By performing variance analysis on categorical columns before hot encoding I can reduce the number of features

![Boxplot for Categorical](https://github.com/Mr-Ahmad-Khalil/Predicting-House-Price-Ames-Dataset-/blob/main/Images/boxplot_categorical.png)


Finally these are the features selected for modelling:

1. SalePrice (target Value)	
2. Overall Qual	
3. Exter Qual	
4. Gr Liv Area	
5. Kitchen Qual	
6. Bsmt Qual	
7. Garage Cars_3.0	
8. 1st Flr SF	
9. Year Built	
10. Garage Finish	
11. Year Remod/Add	
12. Fireplace Qu	
13. Full Bath	
14. Foundation_PConc	
15. TotRms AbvGrd


## 4. Modelling & Evaluation

Original Features shape:

|Data|Columns|Rows|
|----|-------|----|
|Train|14    |1538|
|Test|14     |513|

Modelling:
|Model name|RMSE_train|RMSE_test|RMSE_diff|
|----------|----------|---------|---------|
|Linear Regression|34130|28455 |19.9%|
|RidgeCV| 34198 | 29100 | 17.5%|
|LassoCV| 34130 | 28459 | 19.9%|

The model is badly overfitted that will dealt later in future projects.

Conclusion RidgeCv has the best score.

To choose the top 3 features using the coeeficients from the model RidgeCV:

|Feature Names|Coefficients|
|-------------|------------|
|Gr Liv Area	|146613.995585|
|1st Flr SF	|112830.565273|
|Overall Qual|	98409.973532|
|Exter Qual|	45910.792020|
|Garage Cars_3.0|	43021.029693|
|Bsmt Qual	|38008.550789|
|Kitchen Qual	|37079.532438|
|TotRms AbvGrd|	26386.897771|
|Fireplace Qu	|21102.101941|
|Year Built	|19969.575584|
|Garage Finish	|13886.866758|
|Year Remod/Add	|6673.988134|
|Full Bath	|169.325370|
|Foundation_PConc|	-2762.052249|



## 5. Conclusion & Summary

- The preferred model for predicting is RidgeCV with a scoring difference of 17%. 
- However the model can be improved if given time to do a polynomial to selected features with high correlation with each other.

- In conclusion the top 3 features that have great impact in house prices are:
1. Ground Living Area
2. 1st Floor SquareFeet
3. Overall Quality


(Basically means the bigger the area the higher the price generally.)

- In addition there are features in the house that can be improved that will have a significant increase in the house price such as the Basement Quality and Kitchen Quality.




