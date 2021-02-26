# CST383 Data Science

## Introduction 

### Why was the project undertaken
_According to the CDC, about 655,000 Americans die from heart disease: which is one in every 4 American's die from heart disease. This is one person every 36 seconds. By understanding the features that affect the disease, it is important_

### What was the research question, the tested hypotheseis or purpose of the research? 
_We hypothesized that age, high blood pressure, and sex were some of the leading factors for cardiovascular disease.  We tested this hypotheses and found that there were other factors unknown to us that contributed highly to the probability of dying from cardiovascular disease._ 

### Selection of Data 
_What is the source of the dataset? Characteristics of data?
Any munging or feature engineering?_

_The source of the dataset was from the University of California, Irvine - which used clinical records of heart failure. The characteristics of the data included various features relating to heart disease. The data contained 229 columns and 13 medical features relating to heart disease. This data does not have NA values. The dataset documentation suggested that the feature of time was not a reliable feature._

### Methods
_What materials/APIs/tools were used or who was included in answering the research question?_

1. In the first test case we used a heatmap to determine the top most correlated features relating to death, as well as the top most negative correllated features. A decision tree was used produce a visual of the test case.

2. The second case uses a decision tree model along with the greedy algorithm to find the features that give the highest accuracy. 

3. The third test case uses a decision tree classification model along with a grid search to fine tune the hyperparameters. 

Finally, the final model was created using a decision tree classification model.

### Results
_What answer was found to the research question; what did the study find? Was the tested hypothesis true? Any visualizations?_ 

5 most correlated features are 'age', 'high_blood_pressure', 'serum_creatinine', 'ejection_fraction', 'serum_sodium'. We found that these features were the most highly correlated and based on these features, one's probability of dying from cardiovascular disease was highly affected.


Initially we found that there was a strong correlation between dying of cardiovascular disease with high blood pressure, serum creatine, ejection fraction, and serum sodium based on looking at the heatmap. 

### Discussion
_What might the answer imply and why does it matter? How does it fit in with what other researchers have found? What are the perspectives for future research? Survey about the tools investigated for this assignment._

Implications show that one's age, high blood-pressure, serum creatinine, ejection fraction, and serum sodium are highly impactful to one's heart health. According to the CDC, high blood-pressue is a major risk factor for heart disease (CDC).

Other research shows that unhealthy blood cholesterol levels are a major factor, however cholesterol was not a factor listed in the data collected in our dataset. We noted that there was high variance in our final model, and by adding more data to this model, we can close the gap between training score and cross validation score. 

According to heart.org, the ejection fraction the percent measurement of how much blood the left ventricle pumps out with each contraction (heart.org). Normal range for heart's ejection fraction may be between 50 and 70 percent. 

Serum creatinine measured by doctors to measure renal function. According to WebMD, creatinine levels for a healthy young person is about 95 milliliters (mL) per minute, for women and men the levels should be between 95 to 120 mL. This means that in each minute, a person's kidney clear 95 to 120 mL of blood free of creatinine.


### Summary







