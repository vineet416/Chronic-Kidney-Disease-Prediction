# Chronic-Kidney-Disease-Prediction
The goal of this project is predit the chronic kidney disease using parameters such as 'sugar', 'bacteria', 'blood_glucose_random', 'blood_urea',, 'white_blood_cell_count', 'hypertension', 'diabetes_mellitus', 'coronary_artery_disease', etc.

# Description  
Domain : Healthcare  
Technology:- EDA, Feature Engineering, Feature Selection and Machine Learning  
Languages:- python  

Libraries used:-  
Pandas
Numpy
Matplotlib
Seaborn
Plotly
Sklearn

## 1. Dataset:- Kidney_data.csv  
This dataset can be used to predict the chronic kidney disease and it can be collected from the hospital nearly 2 months of period.  

### Attributes in given data set:-  
age - age  
bp - blood pressure  
sg - specific gravity  
al - albumin  
su - sugar  
rbc - red blood cells  
pc - pus cell  
pcc - pus cell clumps  
ba - bacteria  
bgr - blood glucose random  
bu - blood urea  
sc - serum creatinine  
sod - sodium  
pot - potassium  
hemo - hemoglobin  
pcv - packed cell volume  
wc - white blood cell count  
rc - red blood cell count  
htn - hypertension  
dm - diabetes mellitus  
cad - coronary artery disease  
appet - appetite  
pe - pedal edema  
ane - anemia  
class - class  

## 2. Data Cleaning  
Steps followed during data cleaning:-  
1. Replace all the column names with their full name for better understanding.  
2. Replace categorical values into numerical values.  
3. Correct the mis-spelled categorical values.  
4. Replaced the null values with median for numerical columns and mode for categorical columns.  
5. Removing Duplicated rows.  

## 3. Exploratory Data Analysis  and Data Pre-Processing  
Steps followed in EDA:-    
1. Performed Univariate Analysis, Bivariate and Multivariate Analysis to Understand the data and find some patterns.  
2. Prepared data for model training by converting all categorical columns to numerical using LabelEncoder.  
3. Feature Selection using Variance Inflation Factor (VIF).  
5. DIVIDE THE DATA INTO X (Independent variable), y (target variable / dependent variable).  
6. Spilt the 80 % data for training and 20% data for testing.  

## 5. Creation of machine learning model  
Machine Learning models are created by following Algorithms     
1. Logistic Regression  
2. Decision Tree Classifier  
3. SVM Classifier  
4. Gaussian Naive Bayes  
5. Random Forest Classifier  
6. Ada Boost Classifier  
7. Gradient Boosting Classifier    
8. XG Boost Classifier  

## 6. Hyperparameter tunning  
Perform the hyperparameter tuning to avoid the overfitting in model.     
![image](https://github.com/user-attachments/assets/fa36120a-fc29-4e33-9323-3431504b6d85)


We got 97.5% accuracy score in SVM, XGBoost Classifier, Ada Boost Classifier, and Random Forest Classifier  


