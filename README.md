# Drug-Classification using Machine Learning Models

This project focuses on developing a predictive model to classify drug types that are suitable for patients based on clinical and demographic variables such as Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio as they play an important role in determining the appropriate drug prescriptions to be used. The dataset was preprocessed, exploratory data analysis (EDA) performed and data was visualized using various visualization tools such as pie chart, barplot, scatterplot, heatmap etc. EDA helped to visualize the relationships that existed between the features (Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio) and uncover the trends that determines drug selection. Various machine learning algorithms such as Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees, Random Forest, Support Vector Machines (SVM), XGBoost, LightGBM, and CatBoost were used to train the dataset and their performances were evaluated based on metrics such as accuracy, precision, F1-score and recall.


### Project Visualizations

##### EDA Analysis

###### (i) Bivariate Analysis

<img width="1205" height="346" alt="Screenshot 2026-02-03 175127" src="https://github.com/user-attachments/assets/127c5165-60d9-411c-9d18-55b44f3650f2" />

The distribution analysis shows that DrugY is the most commonly prescribed medication across sexes, blood pressure categories, and cholesterol levels, with a slightly higher prescription rate among females. Across blood pressure groups, DrugY is consistently prescribed for high, low, and normal BP, while DrugX is more frequently prescribed in individuals with normal blood pressure. Similarly, DrugY is used across both high and normal cholesterol levels, indicating that it functions as a first-line treatment regardless of lipid status.



###### (i) Correlation Matrix

<img width="537" height="457" alt="Screenshot 2026-02-03 154024" src="https://github.com/user-attachments/assets/8e7b26ba-6b86-45d5-904e-e0b7e92dd513" />

The correlation matrix illustrated the linear relationships among demographic, clinical, and biochemical variables and their association with the target drug class. The sodium-to-potassium ratio shows the strongest relationship with the drug outcome (r = −0.69), indicating a strong negative correlation and highlighting Na_to_K as a key determinant in drug prescription. Blood pressure exhibited a moderate positive correlation with the drug variable (r = 0.42), further identifying it as an important predictive feature. In contrast, age, sex, and cholesterol displayed weak correlations with the drug outcome (r ≈ 0.02–0.05), suggesting they contributed minimally to drug classification compared with Na_to_K and blood pressure.

###### (ii) Joint Plot Grid 

<img width="489" height="367" alt="Screenshot 2026-02-03 161237" src="https://github.com/user-attachments/assets/b6318750-e5c8-4ed6-bdfb-b26b6c43fdb9" />

The joint plot grid visualized relationships between Age and Na_to_K Ratio, colored by Drug category, with diagonal density plots and off-diagonal scatter plots.

###### (iii) 
