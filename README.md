# Drug-Classification using Machine Learning Models

This project focuses on developing a predictive model to classify drug types that are suitable for patients based on clinical and demographic variables such as Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio as they play an important role in determining the appropriate drug prescriptions to be used. The dataset was preprocessed, exploratory data analysis (EDA) performed and data was visualized using various visualization tools such as pie chart, barplot, scatterplot, heatmap etc. EDA helped to visualize the relationships that existed between the features (Age, Sex, Blood Pressure (BP), Cholesterol levels, and the Sodium-to-Potassium (Na_to_K) ratio) and uncover the trends that determines drug selection. Various machine learning algorithms such as Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees, Random Forest, Support Vector Machines (SVM), XGBoost, LightGBM, and CatBoost were used to train the dataset and their performances were evaluated based on metrics such as accuracy, precision, F1-score and recall.


### Project Visualizations

##### EDA Analysis
#####  (i) Univariate Analysis

<img width="735" height="333" alt="Screenshot 2026-02-04 050312" src="https://github.com/user-attachments/assets/cd3c1fcf-4c0d-447a-9d8c-d4b0fd1447d1" />


These four histograms display the distributions of key health variables in the dataset. The Age Distribution showed relatively uniform spread across 20-80 years with slight peaks in the 25-45 range, indicating balanced age representation. Cholesterol is split nearly equally between HIGH (~100) and NORMAL (~95) categories. The Na_to_K Ratio exhibited right-skewed distribution peaking at ~10 with ~55 individuals and declining toward 35. The Drug Distribution revealed class imbalance with Drug 0.0 dominating (~90 individuals), Drug 4.0 at ~55, and Drugs 1.0-3.0 at progressively lower frequencies (~23, ~16, ~15)

###### (ii) Bivariate Analysis

<img width="1205" height="346" alt="Screenshot 2026-02-03 175127" src="https://github.com/user-attachments/assets/127c5165-60d9-411c-9d18-55b44f3650f2" />

The distribution analysis shows that DrugY is the most commonly prescribed medication across sexes, blood pressure categories, and cholesterol levels, with a slightly higher prescription rate among females. Across blood pressure groups, DrugY is consistently prescribed for high, low, and normal BP, while DrugX is more frequently prescribed in individuals with normal blood pressure. Similarly, DrugY is used across both high and normal cholesterol levels, indicating that it functions as a first-line treatment regardless of lipid status.


###### (iii) Correlation Matrix

<img width="537" height="457" alt="Screenshot 2026-02-03 154024" src="https://github.com/user-attachments/assets/8e7b26ba-6b86-45d5-904e-e0b7e92dd513" />

The correlation matrix illustrated the linear relationships among demographic, clinical, and biochemical variables and their association with the target drug class. The sodium-to-potassium ratio shows the strongest relationship with the drug outcome (r = −0.69), indicating a strong negative correlation and highlighting Na_to_K as a key determinant in drug prescription. Blood pressure exhibited a moderate positive correlation with the drug variable (r = 0.42), further identifying it as an important predictive feature. In contrast, age, sex, and cholesterol displayed weak correlations with the drug outcome (r ≈ 0.02–0.05), suggesting they contributed minimally to drug classification compared with Na_to_K and blood pressure.

###### (iv) Joint Plot Grid 

<img width="489" height="367" alt="Screenshot 2026-02-03 161237" src="https://github.com/user-attachments/assets/b6318750-e5c8-4ed6-bdfb-b26b6c43fdb9" />

The joint plot grid visualized relationships between Age and Na_to_K Ratio, colored by Drug category, with diagonal density plots and off-diagonal scatter plots.

###### (v) Drug Distribution

<img width="1118" height="345" alt="Screenshot 2026-02-04 044050" src="https://github.com/user-attachments/assets/9df11767-fd29-45fa-bc4d-53c4f0b90b22" />

The analysis shows a highly imbalanced drug distribution, with DrugY being the most commonly administered, accounting for about 90 cases and nearly half of all observations (45.5%), followed by DrugX with roughly 55 cases (27.0%), while DrugA, DrugB, and DrugC appear far less frequently. This dominance suggests DrugY may have broader applicability or greater availability. Age distribution patterns further reveal distinct prescribing trends: DrugY and DrugX are used across wide age ranges, indicating suitability for diverse populations, whereas DrugA is concentrated among middle-aged users. DrugC tends to be prescribed to younger individuals, while DrugB is predominantly used by older adults, as reflected by its higher median age and narrower age spread. Together, these findings highlight both usage imbalance across drugs and age-specific prescribing behaviors

### Model Performance

<img width="352" height="174" alt="Screenshot 2026-02-04 042734" src="https://github.com/user-attachments/assets/ab5e2a4b-5009-42e5-8c79-0976643e462e" />

The table shows a clear performance hierarchy across classification models, with tree-based and ensemble methods substantially outperforming linear and distance-based approaches. Decision Tree, Bagging, AdaBoost, and CatBoost achieved near-perfect and identical performance, each reaching 99.38% accuracy with equally high precision, recall, and F1-scores, indicating excellent class separation and highly consistent predictions. Random Forest, LightGBM, and XGBoost also performed strongly, with accuracies above 97%, though slightly lower than the top ensemble group, suggesting marginally reduced generalization or sensitivity to data structure. Extra Trees maintained solid but lower performance at 95%, while probabilistic and linear models (Gaussian Naive Bayes, SGD, and Logistic Regression) showed moderate accuracy, reflecting their limited capacity to capture complex nonlinear patterns. Support Vector Classifier and KNN performed the weakest, indicating that margin-based and distance-based methods were less suited to the underlying feature space. Overall, the results highlight that the dataset is best modeled using tree-based ensemble methods, which effectively capture nonlinear relationships and interactions, yielding superior predictive performance.


### Conclusion

The analysis reveals that DrugY dominates prescription patterns and is broadly applicable across demographic and clinical categories. Drug selection is primarily driven by metabolic (Na_to_K ratio) and blood pressure variables, while age, sex, and cholesterol play minor roles. From a predictive modeling perspective, ensemble and tree-based algorithms achieve near-perfect classification accuracy, demonstrating that the dataset contains strong, structured decision boundaries that can be effectively captured using nonlinear models. Collectively, the findings suggest a highly predictable drug assignment framework driven by key physiological indicators, with DrugY serving as the primary therapeutic option across diverse patient profiles.
