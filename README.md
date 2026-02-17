# Drug-Classification using Machine Learning Models

This project focuses on developing a predictive model to classify drug types that are suitable for patients based on clinical and demographic variables such as Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio as they play an important role in determining the appropriate drug prescriptions to be used. The dataset was preprocessed, exploratory data analysis (EDA) performed and data was visualized using various visualization tools such as pie chart, barplot, scatterplot, heatmap etc. EDA helped to visualize the relationships that existed between the features (Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio) and uncover the trends that determines drug selection. Various machine learning algorithms such as Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees, Random Forest, Support Vector Machines (SVM), XGBoost, LightGBM, and CatBoost were used to train the dataset and their performances were evaluated based on metrics such as accuracy, precision, F1-score and recall.


### Project Visualizations

##### EDA Analysis
#####  (i) Univariate Analysis

<img width="735" height="333" alt="Screenshot 2026-02-04 050312" src="https://github.com/user-attachments/assets/cd3c1fcf-4c0d-447a-9d8c-d4b0fd1447d1" />

The four histograms showed key health variable distributions. Age was fairly evenly spread from 20–80, with a higher concentration between 25–45 while cholesterol levels were roughly half HIGH and half NORMAL. The Na-to-K ratio was right-skewed, peaking around 10 and declining toward 35. Drug use was imbalanced, with Drug 0.0 being the most common, followed by Drug 4.0, while Drugs 1.0–3.0 occurred much less frequently.


###### (ii) Bivariate Analysis

<img width="1205" height="346" alt="Screenshot 2026-02-03 175127" src="https://github.com/user-attachments/assets/127c5165-60d9-411c-9d18-55b44f3650f2" />

The analysis showed that DrugY is the most commonly prescribed medication for both sexes and all blood pressure and cholesterol levels, with slightly more prescriptions for females. DrugY was given to people with high, low, or normal blood pressure, while DrugX was mostly used for normal blood pressure. DrugY was also used for both high and normal cholesterol, showing it is a common first-choice treatment regardless of blood pressure or cholesterol.


###### (iii) Correlation Matrix

<img width="537" height="457" alt="Screenshot 2026-02-03 154024" src="https://github.com/user-attachments/assets/8e7b26ba-6b86-45d5-904e-e0b7e92dd513" />

The correlation matrix showed how demographic, clinical, and biochemical variables related to drug type. The sodium-to-potassium ratio had the strongest link, with a strong negative correlation (r = −0.69), making it a key factor in prescriptions. Blood pressure was a moderate positive correlation (r = 0.42), while age, sex, and cholesterol had very weak correlations (r ≈ 0.02–0.05), meaning they played a minor role in predicting drug type.


###### (iv) Joint Plot Grid 

<img width="489" height="367" alt="Screenshot 2026-02-03 161237" src="https://github.com/user-attachments/assets/b6318750-e5c8-4ed6-bdfb-b26b6c43fdb9" />

The joint plot grid visualized relationships between Age and Na_to_K Ratio, colored by Drug category, with diagonal density plots and off-diagonal scatter plots.

###### (v) Drug Distribution

<img width="1118" height="345" alt="Screenshot 2026-02-04 044050" src="https://github.com/user-attachments/assets/9df11767-fd29-45fa-bc4d-53c4f0b90b22" />

The analysis showed that DrugY was used the most, with 90 cases (45.5%), followed by DrugX with 55 cases (27%), while DrugA, DrugB, and DrugC were much less common. This suggested that DrugY was more widely used or more available. DrugY and DrugX were prescribed across many age groups, while DrugA was mostly used by middle-aged people. DrugC was more common in younger individuals, and DrugB was mainly prescribed to older adults. Overall, the results showed an imbalance in drug use and clear age-based prescribing patterns.

### Model Performance

<img width="352" height="174" alt="Screenshot 2026-02-04 042734" src="https://github.com/user-attachments/assets/ab5e2a4b-5009-42e5-8c79-0976643e462e" />

The table shows a clear performance hierarchy across classification models, with tree-based and ensemble methods substantially outperforming linear and distance-based approaches. Decision Tree, Bagging, AdaBoost, and CatBoost achieved near-perfect and identical performance, each reaching 99.38% accuracy with equally high precision, recall, and F1-scores, indicating excellent class separation and highly consistent predictions. Random Forest, LightGBM, and XGBoost also performed strongly, with accuracies above 97%, though slightly lower than the top ensemble group, suggesting marginally reduced generalization or sensitivity to data structure. Extra Trees maintained solid but lower performance at 95%, while probabilistic and linear models (Gaussian Naive Bayes, SGD, and Logistic Regression) showed moderate accuracy, reflecting their limited capacity to capture complex nonlinear patterns. Support Vector Classifier and KNN performed the weakest, indicating that margin-based and distance-based methods were less suited to the underlying feature space. Overall, the results highlight that the dataset is best modeled using tree-based ensemble methods, which effectively capture nonlinear relationships and interactions, yielding superior predictive performance.


### Conclusion

The table showed that tree-based and ensemble models performed much better than linear and distance-based models. Decision Tree, Bagging, AdaBoost, and CatBoost achieved almost perfect results (99.38% accuracy) with very high precision, recall, and F1-scores. Random Forest, LightGBM, and XGBoost also performed very well, with accuracy above 97%. Extra Trees had slightly lower performance at 95%. Linear and probabilistic models like Logistic Regression, SGD, and Naive Bayes had moderate accuracy, while SVC and KNN performed the weakest. Overall, tree-based ensemble methods work best for this dataset because they captured complex patterns and relationships more effectively.


