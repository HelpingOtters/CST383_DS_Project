# My Achey-Breaky Heart
## By the Helping Otters (Ricardo Barbosa, Max Halbert, Lindsey Reynolds & Dan Sedano)

[Video Demo on YouTube](https://youtu.be/q4HZhBLZkP4)
## Introduction 
_Why was the project undertaken?_

According to the CDC, about 655,000 Americans die from heart disease every year, which is 1 in every 4 Americans. This is one person every 36 seconds. By knowing the risk factors for cardiovascular disease, one can make better choices to avoid heart failure. 

_What was the research question, the tested hypothesis or purpose of the research?_

We originally hypothesized that age, high blood pressure, and sex were some of the leading factors for cardiovascular disease. We tested this hypothesis and found that there were other factors unknown to us that contributed highly to the probability of dying from cardiovascular disease.
Based on the initial raw data visualization, specifically the heatmap, we updated our hypothesis to say that high levels of serum creatinine, age, ejection fraction, and serum sodium would increase the likelihood of cardiovascular disease.

## Research question: What is the percent likelihood of someone dying from cardiovascular disease based on specific high impact risk factors?

## Selection of Data 
_What is the source of the dataset? Characteristics of data?_

The source of our dataset is the University of California, Irvine.
Our data includes 299 clinical records, including 13 medical features relating to heart disease.
This dataset has no N/A values
Any munging or feature engineering?
We did not need to do any feature engineering
The dataset documentation suggested that the feature of time was not a reliable feature, so we dropped it from our dataset.

## Methods 
_What materials/APIs/tools were used or who was included in answering the research question?_

In order to complete this project, we used Kaggle to find and download our dataset to github.
We then used Google Colab in order to create our model and visualize, manipulate and understand our data. 

## Walk Through Data Visualization
First we plotted a heat map
Most negatively correlated features: ejection fraction and serum sodium
Most positively correlated features: age and serum creatinine
Plotted a histogram of ejection fraction to see how it affected death count
Found that lower levels of ejection fraction resulted in a higher death count
According to heart.org, ejection fraction is the percentage of blood that the left ventricle pumps out with each contraction (heart.org). Normal range is between 50 and 70 percent.
Plotted histogram of serum creatinine and how it affects death count
Found that lower levels of serum creatinine resulted in a higher death count
Serum creatinine is used to measure renal or kidney function.
Plotted both of these highly correlated features onto one graph to see how they were both related to death events


### First Test Case 
Used 2 most negatively correlated features and 3 most positively correlated features from the heatmap
We used trial and error to determine that a max depth of 3 and minimum sample split of 10 gave us the most accurate results. 
We found that some of our leaf node’s sample sizes were as small as 0.4%, which may indicate overfitting. Because of this, we will add another hyperparameter, minimum sample leaf, to avoid this as we tune our model.
We also found that the most important features in this model were age, serum creatinine, ejection fraction and serum sodium. 

### Second Test Case 
In order to further fine tune our model, we decided to use a greedy algorithm to determine the best features. 
When we ran our algorithm, we found that after just two features were added, the accuracy of the model no longer improved. 
Those two features turned out to be ejection fraction and serum creatinine. We used these two features to create our second test model.
Looking at the cross tab graph, we can see that our accuracy has improved compared to our first test model. 

### Third Test Case 
Once we knew which features to use in our model, we decided to use grid search in order to fine tune our hyperparameters
This came back saying that a max depth of 2 and minimum sample split of 2 were the best hyperparameters
Looking at the cross tab graph, however, it is clear that this model gives a high number of false negatives and is not providing higher accuracy than our previous test model. 

### Final Model (Results)
Based on our three test models, it is clear that our second test model was the most accurate. This model used the two most correlated features, a max depth of 3 and minimum sample leaf of 10.
Using our final model, we were able to test our hypothesis by running predictions using example test data.
Each test case provides the percent likelihood of death given the sample data. 


## Discussion 
_What might the answer imply and why does it matter?_

Our final result implies that a person’s serum creatinine levels and ejection fraction levels are the most impactful risk factors. Age and high blood-pressure were not as influential as we initially hypothesized.

_How does it fit in with what other researchers have found?_

According to the CDC, high blood-pressure is a major risk factor for heart disease (CDC). Our data shows a correlation as well, but we did not find that it was the major factor.
Other research also shows that unhealthy blood cholesterol levels are a major factor, however cholesterol was not a factor listed in the data collected in our dataset. 

_What are the perspectives for future research?_

Because our dataset was so small, it was hard to determine exactly how impactful some of the other features were. For future research, we feel that increasing the size of the training data would allow for more accuracy and exploration. 
Survey about the tools investigated for this assignment.
We chose to use Google Colab for this assignment because it was easy to work with for a group project. We were able to work at the same time and easily see updates in comparison to other development environments. 

## Summary 
_Most important findings_

Serum creatinine and ejection fraction were the most impactful features in terms of increasing the accuracy of our model.

_Further Research_

Our model has high variance, which indicates that it may be too flexible 
We need more data in order to close the gap between the test and training set accuracy

## Citations/Bibliography

“Know Your Risk for Heart Disease.” Centers for Disease Control and Prevention, Centers for Disease Control and Prevention, 9 Dec. 2019, www.cdc.gov/heartdisease/risk_factors.htm.

“Heart and Stroke Encyclopedia.” Heart, www.heart.org/HEARTORG/Encyclopedia/Heart-and-Stroke-Encyclopedia_UCM_445084_ContentIndex.jsp?title=creatinine. 

“Creatinine Clearance Blood Test: Purpose, Procedure, Results.” WebMD, WebMD, 28 July 2020, www.webmd.com/a-to-z-guides/creatinine-and-creatinine-clearance-blood-tests. 








