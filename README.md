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

## 7. Model Evaluation  

![image](https://github.com/user-attachments/assets/9855c146-e3c3-474e-84db-67db6d0ccf3f)


![image](https://github.com/user-attachments/assets/fa36120a-fc29-4e33-9323-3431504b6d85)


We got 97.5% accuracy score in SVM, XGBoost Classifier, Ada Boost Classifier, and Random Forest Classifier  



# Insights    
## EDA and Feature Engineering:  
1. Demographics and Symptoms:    
   - CKD predominantly affects older individuals, with blood pressure increasing significantly with age.        
   - Symptoms like peda edema, poor appetite (in 20.6% of cases), and anemia are common among CKD patients.
   
2. Co-Morbidities:    
   - A strong correlation exists between diabetes mellitus, hypertension, and CKD, highlighting their combined influence on kidney health.        
   - 34.4% of the dataset shows individuals with diabetes, and a significant number of these also exhibit hypertension.    

3. **Biomarkers**:    
   - Serum creatinine and blood urea levels are markedly higher in CKD-positive cases, with significant outliers indicating varying stages of the disease.    
   - Elevated albumin levels in individuals with diabetes suggest kidney damage as a direct result of the condition.    

4. **Feature Selection**:    
   - Age, blood pressure, albumin, sugar, serum creatinine, and diabetes mellitus were identified as the most impactful features for CKD prediction.    


## Model Training and Evaluation:
1. Model Performance:
   - SVM Classifier and XGBoost Classifier achieved the highest accuracy (97.5%), effectively handling the complex relationships in the dataset.
   - Ensemble models like Random Forest and AdaBoost delivered 97.5% accuracy, indicating strong predictive capabilities.

2. Impact of Hyperparameter Tuning:
   - Fine-tuning parameters significantly improved accuracy across models:
     - SVM Classifier: Improved from 91.25% to 97.5%
     - Logistic Regression: Improved from 90% to 96.25%.
     - Gradient Boosting and AdaBoost showed enhanced generalization after tuning.

3. Evaluation Metrics:
   - Models consistently showed balanced precision, recall, and F1-scores, with minimal false negatives, essential for early CKD diagnosis.

4. Overfitting:
   - Ensemble models showed slight overfitting, as evidenced by near-perfect training accuracy compared to test accuracy, requiring further validation on external datasets.


# Summary
- Key Insights:
  - Diabetes mellitus, hypertension, and elevated serum creatinine are critical factors influencing CKD.
  - Ensemble models, especially XGBoost, excel in predictive accuracy and reliability for CKD detection.
  - Age-specific trends (e.g., rising blood pressure with age) and symptoms like anemia and peda edema provide valuable clinical insights.

- Workflow:
  - The project followed a structured pipeline:
    1. Data cleaning
    2. Comprehensive exploratory analysis.
    3. feature engineering and Preprocessing.
    4. Model training and hyperparameter tuning.


# Conclusion
1. Critical Drivers:
   - Biomarkers like serum creatinine, albumin, and blood urea are key predictors of CKD, with age, hypertension, and diabetes serving as significant contributing factors.
   - Co-morbidities should be monitored closely for early intervention.

2. Model Deployment:
   - XGBoost, with its superior accuracy, is recommended for real-world CKD prediction systems.
   - SVM Classifier, Random Forest and AdaBoost can serve as robust alternatives, offering high performance and interpretability.

3. Future Directions:
   - External validation on larger datasets to improve model generalization.
   - Development of lightweight models for deployment in resource-limited settings.
   - Collaboration with medical professionals to enhance model explainability and utility in clinical workflows.


# 📩 Feedback
If you have any feedback, please reach out to me at Linkedin: https://www.linkedin.com/in/vineet-patel416/
