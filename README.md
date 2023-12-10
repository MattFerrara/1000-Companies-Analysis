
# 1000 Companies Data Analysis

## Introduction

In this project, I use data from 1000 companies to predict their profit outcomes. My goal is to provide a data-driven solution using tools like NumPy, SciPy, Pandas, and Scikit-learn. The excitement lies in uncovering valuable insights from the dataset and building a reliable predictive model.

I opted for the simplicity of linear regression, aiming to capture the relationships between various features and company profits. Preprocessing tools like OneHotEncoder, StandardScaler, PolynomialFeatures, and SimpleImputer enhance the model's performance. 

A streamlined pipeline ensures consistency, and GridSearchCV fine-tunes hyperparameters for optimal results.

## Selection of Data
The model processing and training are conducted using a Jupyter Notebook and is available under the code section. R&D Spending, Administration, Marketing Spend, State and Profit.

The objective is to predict the future profits of the companies. The dataset can be found online at Kaggle[1]

Data preview:

![image](https://github.com/MattFerrara/1000-Companies-Analysis/assets/90582699/afafb521-3d70-4996-af3b-f9134c53ee10)


Note that the data has one categorical feature in column 4 which is: 'State'
The data consist of 1000 rows with 6 different columns: 
## Methods
My tools:

NumPy, Pandas, and the Scikit-learn for data regression and analysis
Github
Jupyter as IDE

Inference methods used with SciKit
Linear regression model
	 Hahahaha
Features: OneHotEncoder/ColumnTransformer, StandardScaler, PolynomialFeatures and SimpleImputer for missing data 
OneHotEncoder: transforms categorical variables(“State”) into binary vectors, making them suitable for machine learning algorithms.

ColumnTransformer: applies different transformers to different subsets of features, allowing for a streamlined and organized preprocessing workflow.

Standard Scaler: utilized to standardize numerical features by removing the mean and scaling to unit variance.

Polynomial Features: This is applied to create polynomial features from the original features. By introducing polynomial terms, the model can capture more complex patterns in the data.

SimpleImputer: This is used for handling missing values in the dataset. It allows for various strategies to fill in missing values, such as mean, median, or constant values. 
PipeLine
A pipeline ties all these preprocessing steps together in a sequence. This ensures that the same transformations are applied consistently to both the training and testing datasets. The pipeline simplifies the workflow and makes code readable, making it easier to maintain and reproduce.

GridSearchCV: The entire workflow is organized using pipelines, and hyperparameter tuning is performed using GridSearchCV to optimize the model's performance.
## Results
In the first experiment I didn’t expect to get such a high linear regression score
This came out to be a .949 accuracy rate. This is considered to be a very good accurate score. 
INSERT IMAGE.
Then I did a second experiment to see if I could get the results even closer to 100% using pipeline preprocessing methods. I came out to a test Score of .985 which is almost 100%. 
INSERT IMAGE

After that I used GridSearchCV to find the best grid search for the data which came out to approximately .959
INSERT IMAGE

## Discussion
Experimenting with various feature engineering and techniques and regression algorithmsI found that linear regression with one hot encoding provided a super high accuracy. Across all of my trials, my training accuracy was around 94% while my training score was 96%. Thus I wanted to try to  get to 100% since I was already so close with just the linear regression model alone. The data was split using a test size of .2, which is 80/20 for testing and has a testing accuracy of 98%.
Kaggle didn’t have any notebooks on this data but I did note that it had 0 missing data items, which made the whole thing a whole lot easier.

## Summary
This project deployed a regression model to predict profits of a company based on 5 different features. After experimenting with various feature engineering techniques, the deployed model’s testing accuracy was approximately 98%.

## References
[1]https://www.kaggle.com/datasets/sadikaljarif/1000-companiescsv
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html
