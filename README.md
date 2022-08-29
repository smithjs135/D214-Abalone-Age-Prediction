# D214-Abalone-Age-Prediction
Using Random Forest Regression to Predict the Age of an Abalone

## Research Question

Can the age of an abalone be predicted based on an abalone’s 'Sex', 'Diameter', and 'Whole weight'? 
The age of an abalone is currently determined by shucking and cutting the shell then counting the number of growth rings contained in the shell.  Shucking the abalone shell kills the animal.  The purpose of this analysis is to accurately determine the age of an abalone without killing it. 
The working hypothesis is the variables 'Sex', 'Diameter' and 'Whole weight' statistically significantly affect the variable 'Age'.
As an abalone gets older, it grows additional growth rings which should reflect an increase in shell diameter and weight of the animal.

##Data Collection
This analysis will use the Abalone Dataset from Kaggle (Mendes, 2018). The advantage of using this data is that it is readily available and free to use.  Furthermore, this dataset contains 4,177 rows of data which should be sufficient to show trends in size and weight in relation to an abalone's age. 
The values for diameter and whole weight were recorded in millimeters. These two features were scaled by dividing each value by 200(UCI). The scaled data values are used for this analysis. 

Rings are recorded is whole integer value.  The age is calculated by adding 1.5 to the ring value.
The datatypes of the 3 attributes are float64. 

## Libraries
* pandas
* numpy
* seaborn
* matplotlib

## Environment
* Python version: 3.8.5
* Jupyter Notebook

## Accuracy
The overall accuracy is approximately 82%. This model does show some ability to predict the age of an abalone but is less than desired.

## Data summary and implications
The results of this analysis did not sufficiently support the hypothesis.
The working hypothesis is the variables 'Sex', 'Diameter' and 'Whole weight' statistically significantly affect the variable 'Age'.
A Random Forest Regression model was used to predict the age of an abalone based on its diameter and weight. The dataset was acquired from Kaggle and originally contains 9 columns and 4,177 rows of data. Sklearn.model_selection was used to split the data into train and test datasets. The Sklearn.ensemble package was used to run the Random Forest Regression algorithm. This model displayed an accuracy of 81.87%. This value of accuracy demonstrates some ability to predict the age of an abalone but not to the desired level.
The accuracy can likely be improved incrementally several ways. 
(1)An abalone’s weight may differ for males and females. Reapplying the model to the dataset that is filtered on either males or females may result in a higher accuracy.   
(2)The features Diameter and Weight both had weak correlations to Age. Running a correlation matrix against the entire dataset may help locate other features with strong correlation values to Age.
(3)Hyper parameters tuning may improve accuracy as well. These parameters include "n_estimators" and max_depth(Datascience Learner). Working with the stakeholders to increase the number of rows of data and including additional data points such as location and amount of food source may also help achieve better insight and accuracy. This is the least desirable of the options because it may only come with added costs and delay to this project.

## Third-Party Code Sources
1.	RODOLFO MENDES (2018). Abalone Dataset https://www.kaggle.com/datasets/rodolfomendes/abalone-dataset (MENDES, 2018)
2.	Rodolfo Mendes(2018). Abalone Dataset. https://www.kaggle.com/datasets/rodolfomendes/abalone-dataset
3.	Sofia Kapsiani & Brendan J. Howlin(Jul, 2021). Random forest classification for predicting lifespan-extending chemical compounds https://www.nature.com/articles/s41598-021-93070-6
4.	Cuemath. Accuracy Formula https://www.cuemath.com/accuracy-formula/
In-Line Sources
1.	UCI. Abalone Data Set. https://archive.ics.uci.edu/ml/datasets/abalone
2.	Aditya Kumar (Jun, 2020). Random Forest for prediction https://towardsdatascience.com/random-forest-ca80e56224c1 (Kumar, 2020)
3.	Data Science Learner. How to Improve Accuracy of Random Forest ? Tune Classifier In 7 Steps https://www.datasciencelearner.com/how-to-improve-accuracy-of-random-forest-classifier/ (Datascience Learner)
