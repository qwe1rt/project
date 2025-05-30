### Project Overview  
    This data mining project aims to build a heart disease risk prediction model based on the Cleveland Heart Disease Dataset (UCI Machine Learning Repository：https://archive.ics.uci.edu/dataset/45/heart+disease). By analyzing patients' medical characteristics (such as age, gender, chest pain type, etc.), the project predicts whether patients are at risk of heart disease. The project covers the complete machine learning workflow, including data preprocessing, feature engineering, model training and evaluation, feature importance analysis, and model deployment.
### Dataset  
Source: UCI Machine Learning Repository - Cleveland Heart Disease Dataset  
Samples: 303  
Features: 13 medical features + 1 target variable  
Target Variable:  0 = No heart disease，1 = Heart disease present  
Feature Examples:  
Age(age)，Sex(sex)，Chest Pain Type(cp)，Resting Blood Pressure(trestbps)，Serum Cholesterol(chol)，Fasting Blood Sugar(fbs)，Resting Electrocardiographic Results(restecg)，Maximum Heart Rate Achieved(thalach)，Exercise-Induced Angina(exang)，ST Depression Induced by Exercise(oldpeak)，Slope of the Peak Exercise ST Segment(slope)，Number of Major Vessels Colored by Fluoroscopy(ca)，Thalassemia(thal)  
### Technical Methods  
Data Preprocessing：  
Missing Value Handling: Fill with median (for numerical features) or mode (for categorical features).  
Numerical Feature Standardization: Use `StandardScaler` for normalization.  
Categorical Feature One-Hot Encoding: Apply `OneHotEncoder` for encoding.  
Class Imbalance Handling: Set `class_weight='balanced'` to address imbalance.  
Model Construction and Evaluation：  
Stratified Sampling: Split the dataset into training/test sets (80%/20%) using stratified sampling.  
Machine Learning Models Evaluated: Logistic Regression，Random Forest，Support Vector Machine (SVM)，Gradient Boosting  
Evaluation Metrics: Accuracy ，Precision ，Recall ，F1-Score ，AUC Value  
#### Feature Importance Analysis  
Visualize feature importance of the best-performing model.  
Identify key risk factors for heart disease.

### Key Results  
Model Performance Comparison  
| Model               | Accuracy | Precision | Recall  | F1-Score | AUC      |  
|---------------------|----------|-----------|---------|----------|----------|  
| Random Forest       | 0.9016   | 0.9091    | 0.9091  | 0.9091   | 0.9653   |  
| Gradient Boosting   | 0.8689   | 0.8889    | 0.8636  | 0.8761   | 0.9304   |  
| Logistic Regression | 0.8525   | 0.8710    | 0.8636  | 0.8673   | 0.9231   |  
| SVM                 | 0.8361   | 0.8400    | 0.8636  | 0.8516   | 0.9070   |  
Best Model: Random Forest
### Key Findings  
Most Important Predictive Features:  Maximum Heart Rate (thalach)，Chest Pain Type (cp) ，Exercise-Induced Angina (exang)，ST Depression (oldpeak) 
Model Advantages:  
High Recall (91%): Effectively identifies patients with heart disease.  
High AUC (0.965): Excellent discriminatory power between positive and negative cases.
### Explanation of Prediction Parameters  
The model requires the following 13 feature parameters for prediction:  
Sex (sex: 0 = Female, 1 = Male)  
Chest Pain Type (cp: 1–4) 
Fasting Blood Sugar (fbs: 0/1) 
Resting Electrocardiographic Results (restecg: 0–2)
Exercise-Induced Angina (exang: 0/1)  
Slope of the Peak Exercise ST Segment (slope: 1–3) 
Number of Major Vessels Colored by Fluoroscopy (ca: 0–3)
Thalassemia (thal: 3 = Normal, 6 = Fixed Defect, 7 = Reversible Defect)
### Conclusions and Recommendations  
Model Applications：  
Serve as an auxiliary tool for medical screening.  
Aid in identifying high-risk patients for early intervention.  
Areas for Improvement：  
Collect more data to enhance model robustness.  
Explore deep learning models.  
Add SHAP value interpretation functionality for better explainability.
