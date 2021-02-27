# CST383 Data Science

## Introduction 

#### Why was the project undertaken?
_According to the CDC, about 655,000 Americans die from heart disease every year, which is 1 in every 4 Americans. This is one person every 36 seconds. By knowing the risk factors for cardiovascular disease, one can make better choices to avoid heart failure._

#### What was the research question, the tested hypotheseis or purpose of the research? 
_Inital Hypothesis: We originally hypothesized that age, high blood pressure, and sex were some of the leading factors for cardiovascular disease.  We tested this hypothesis and found that there were other factors unknown to us that contributed highly to the probability of dying from cardiovascular disease._

_Updated Hypothesis: Based on the initial raw data visualization (specifically the heatmap), we hypothesized that high levels of serum creatinine, age, ejection fraction, and serum sodium would increase the likelihood of cardiovascular disease._

_Research Question: What is the percent likelihood of someone dying from cardiovascular disease based on specific high impact risk factors?_

## Selection of Data 
#### What is the source of the dataset? Characteristics of data?
_The source of our dataset is the University of California, Irvine.
Our data includes 299 clinical records, including 13 medical features relating to heart disease.
This dataset has no N/A values._

#### Any munging or feature engineering?
_We did not need to do any feature engineering
The dataset documentation suggested that the feature of time was not a reliable feature, so we dropped it from our dataset._


## Methods
#### What materials/APIs/tools were used or who was included in answering the research question?
_We used Kaggle to find and download our dataset to github. We then used Google Colab in order to create our model and visualize, manipulate and understand our data._

## Results
#### What answer was found to the research question; what did the study find? Was the tested hypothesis true? Any visualizations?
_We found that the two most correlated features that affect the death rate of heart disease are ejection fraction and serum creatinine. After running these three test models, it was the second case (using a greedy algorithm and max_depth=2) that provided the best result._ 
_The hypothesis that age, high blood pressure and sex were the leading factors associated with heart disease was not proven in our experiment._
_The information we saw in the heatmap, however, did prove to be accurate. The most negatively and positively correlated features provided the most accurate model._

## Discussion
#### What might the answer imply and why does it matter?
_Implications show that one's age, high blood-pressure, serum creatinine, ejection fraction, and serum sodium are highly impactful to one's heart health. According to the CDC, high blood-pressure is a major risk factor for heart disease (CDC)._

#### How does it fit in with what other researchers have found?
_Other research shows that unhealthy blood cholesterol levels are a major factor, however cholesterol was not a factor listed in the data collected in our dataset. We noted that there was high variance in our final model, and by adding more data to this model, we can close the gap between training score and cross validation score._

#### What are the perspectives for future research?
_According to heart.org, the ejection fraction is the percent measurement of how much blood the left ventricle pumps out with each contraction (heart.org). Normal range for the heart's ejection fraction may be between 50 and 70 percent._

#### Survey about the tools investigated for this assignment.
_Serum creatinine measured by doctors to measure renal function. According to WebMD, creatinine levels for a healthy young person is about 95 milliliters (mL) per minute, for women and men the levels should be between 95 to 120 mL. This means that in each minute, a person's kidney clears 95 to 120 mL of blood free of creatinine._


## Summary
#### Most important findings
_Serum_creatinine and ejection_fraction were the most impactful features for our model._

#### Further Research
_Our model has high variance and is too flexible. We need more data in order to close the gap between the test and training set accuracy_







