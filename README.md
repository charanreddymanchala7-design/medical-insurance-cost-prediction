<h1><p align = "center"> Medical Insurance Cost Prediction</p></h1>

## PROJECT OVERVIEW
Health insurance costs have risen dramatically over the past decade in response to the rising cost of health care services and are determined by a multitude of factors. Let's look at the cost of healthcare for a sample of the population given age, sex, bmi, number of children, smoking habits, and region.

The purpose of this project is to determine the contributing factors and predict health insurance cost by performing exploratory data analysis and predictive modeling on the Health Insurance dataset. This project makes use of Numpy, Pandas, Sci-kit learn, and Data Visualization libraries.

Overview:
- Seek insight from the dataset with Exploratory Data Analysis
- Performed Data Processing, Data Engineering and Feature Transformation to prepare data before modeling
- Built a model to predict Insurance Cost based on the features
- Evaluated the model using various Performance Metrics like RMSE, R2, Testing Accuracy, Training Accuracy and MAE

## DATA DESCRIPTION
1. age: age of primary beneficiary
2. sex: insurance contractor gender, female, male
3. bmi: Body mass index, providing an understanding of body, weights that are relatively high or low relative to height, objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9
4. children: Number of children covered by health insurance / Number of dependents
5. smoker: Smoking
6. region: the beneficiary's residential area in the US, northeast, southeast, southwest, northwest
7. charges: Individual medical costs billed by health insurance

Data source: https://www.kaggle.com/mirichoi0218/insurance

## EXPLORATORY DATA ANALYSIS (EDA)
- Feature sex and region has an almost balanced amount, meanwhile most people are non smoker and obese
![image](https://user-images.githubusercontent.com/80570935/130601931-826570ec-df1d-4b85-918f-00eb740ed212.png)

- A person who smoke and have BMI above 30 tends to have a higher medical cost
![image](https://user-images.githubusercontent.com/80570935/130602334-b62a7f7e-e1c8-45eb-be7d-ff752853d158.png)

- Older people who smoke have more expensive charges
![image](https://user-images.githubusercontent.com/80570935/130602565-2cb73fa9-769b-4822-880e-c009d2fbef39.png)

- People who smoke and obese have the highest average charges compared to others
![image](https://user-images.githubusercontent.com/80570935/130602770-c008fb2b-2041-440e-b92e-373e7cbed2ce.png)

## INSIGHTS
The insights drawn by performing "Exploratory Data Analysis" (EDA) are:

- Most people are a non smokers and obese.
- Feature sex and region has an almost balanced amount.
- People who smoke and have a higher BMI, has higher medical charges.
- Older people who smoke have more expensive charges.
- An obese person who smokes have higher charges.

## DATA PROCESSING 
1. Check missing value - there are none
2. Check duplicate value - there are 1 duplicate, will be remove
3. Feature engineering - make a new column "weight_status" based on BMI score
4. Feature transformation:
 A) Encoding "sex", "region", and "weight_status" attributes
 B) Ordinal encoding "smoker" attribute
5. Modeling:
 A) Separating target and features
 B) Splitting train and test data
 C) Modeling using Linear Regression, Random Forest, Decision Tree, Ridge, and Lasso algorithm
 D) Find the best algorithm
 E) Tuning Hyperparameter
 
## MODEL EVALUATION 
| Score | LinearRegression | DecisionTree | RandomForest | Ridge |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| R2 | 0.77 | 0.78 | 0.78 | 0.86 |
| Train Accuracy | 0.74 | 1.0 | 0.97 | 0.74 |
| MAE | 4305.20 | 2798.83 | 2608.55 | 4311.10 |
| Test Accuracy | 0.77 | 0.78 | 0.86 | 0.77 | 
| RMSE | 6209.88 | 6067.50 | 4841.88 | 6238.13 |
 
## CONCLUSION
Based on the predictive modeling, Linear Regression algorithm has the best score compared to the others, with MAE Score 4305.20, RMSE Score 6209.88, and R2 Score 0.77.

Therefore, Linear Regression algorithm is the best fitted model based on the training and testing accuracy.

## MAINTAINER
This repository is maintained by Charan Reddy Manchala.

About the Developer:
Charan is a 5x Certified Salesforce Developer with over 8 years of experience in designing and implementing enterprise-level solutions. With expertise in Apex, LWC, and complex system integrations, he applies a disciplined approach to software development and data analysis. This project serves as a demonstration of applying predictive modeling techniques to healthcare financial data.

Contact Information:
- Email: charanreddymanchala9@gmail.com
- GitHub: charanreddymanchala9
- LinkedIn: charanreddymanchala9