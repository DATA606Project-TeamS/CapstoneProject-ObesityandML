# CapstoneProject
# Analyzing Risk Factors Associated  with Obesity/Overweight Using Machine Learning

## Contributors:


## Project Introduction
Our project aims to analyze the relationship between obesity/overweight and different risk factors such as BMI, Race, Gender, physical activities, mental health, education level, and etc. Obesity constitutes a major public health concern in the U.S. and Globally. About 1 in 5 children and more than 1 in 3 adults struggle with obesity in the U.S. (CDC) Adults with obesity have higher risk for developing Heart disease, Type 2 diabetes, and some types of cancer (CDC) According to the The “World Health Organization” (WHO), 30% of global death will be caused by lifestyle diseases by 2030. From our research, there is a limited number of studies using machine learning to analyze obesity/overweight related datasets in the U.S. Hence, we have chosen to research on different risk factors related to obesity/overweight using data from the U.S.<br/>

![alt text](https://www.cdc.gov/obesity/about-obesity/images/1in5-1in3.jpg)
![alt text](https://www.cdc.gov/obesity/about-obesity/images/higher-risk.jpg)

## Research questions
1. Which variables are risk factors related to obesity/overweight?<br/>
2. What are the correlations between different risk factors and BMI?<br/>
    - Is mental health an important factor that correlates with obesity/overweight?<br/>
3. Which machine learning model can classify and conduct regression of the dataset?<br/>

## Approach
- Conduct EDA to find the relationship of different factors and produce visualizations. <br/>
- Find the most accurate model for our dataset. <br />
- Classification and Regression models (e.g Random Forest, Support Vector Machines (SVM), Logistic Regression, and Decision Trees)<br/>

## Literature/Industry research review
- The Technology and Health Departments of the University of Agder (Norway) identified potential risk factors associated with obesity/overweight using machine learning methods such as Support Vector Machines (SVM), Decision Trees, and Logistic regression models. (Chatterjee et al, 2021)<br/>
- The Daffodil International University in Dhaka (Bangladesh) applied 9 prominent ML algorithms to predict the risk of obesity on the data collected from many varieties of people of different ages suffering from obesity and non-obesity. (Ferdowsy F. et al, 2021)<br/>
- The University of Bologna (Italy) used ML techniques to test for the predictive effects of emotional and affective variables over BMI values. (Delnevo et al, 2021)<br/>
Approach:<br/>
Both classification and Regression models including K-Nearest neighbor, Classification and Regression Tree, support Vector Machine, Multi-Layer Perceptron, Ada boosting with decision tree, Gradient Boosting, Random Forest, LASSO (Least Absolute Shrinkage and Selection Operator), and Elastic Regression. <br/>
Findings:<br/>
Using affect-related variables it is possible to predict the BMI with a good level of accuracy and the psychological variable that had most impact on the predictive capabilities of the algorithms is Depression
The best performance was achieved by the LASSO and Elastic Net, with a MAE (mean absolute error) equal to 4.35 and the PCCs (Pearson correlation coefficient ) respectively of 0.81 and 0.80, indicating a strong correlation between predictions and real value.<br/>

Limitations:<br/>
Restricted number of subjects<br/>
It did not employ newly collected data, thus making inferences limited<br/>
Lack of other factors such as lifestyle habits<br/>





## Dataset Scope
- Source: <br/>
CDC - National Center for Health Statistics. National Health and Nutrition Examination Survey  March 2017 to 2020 Pre-pandemic<br/>
NHANES is a program of studies designed to assess the health and nutritional status of adults and children in the United States. 
The survey is unique in that it combines interviews and physical examinations. <br/>
- Data type (numerical & categorical): <br/>
Demographics data, examination data, laboratory data, & questionnaire data including; Respondent sequence number, Gender, Race, Country of birth, Education level, Ratio of family income to poverty, Body measures(Weight, Height, BMI, BMI category), Diabetes status, Physical activity(Moderate work activity, recreational activity), Mental health(Depressed, Poor appetite or overeating), and Sleep disorders(Sleep hours on weekdays and weekends). <br/>
- Dataset size:<br/>
12.4MB - XPT. files / Zipped data file:1.4 MB<br/>

## Analysis
- Heatmap of risk factors with numerical values. Besides weight and height, we found that Age also has a strong correlation to BMI.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/Heatmap.png)
#### BMI guideline from CDC:<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20guide.png)<br/>
- We found that our dataset contains infants, children, teenagers, adults, and seniors. Thus, we added a new column and separated respondents to different age groups.<br /> Age groups: 0-3, 3-12, 13-19, 20-60, 60+ <br />
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/Age%20groups.png)<br/>
#### Box plot of BMI and Gender:<br/> 
The overall female BMI is slightly higher than male BMI in our dataset.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%26Gender-boxplot.png)
#### Box plot of BMI and Race:<br/> 
We noticed that None-Hispanic Asians have lower BMI.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%26Race-boxplot.png)
#### Box plot of BMI and Education level:<br/> 
People with college degree or above tend to have lower BMI.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%26EducationLevel.png)
#### Bar chart of BMI and Depression:<br/> 
Respondents with depression related experiences tend to have higher BMI compared to others.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%26Depression.png)

## Datasets Used
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Demographics&Cycle=2017-2020
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Examination&Cycle=2017-2020
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Questionnaire&Cycle=2017-2020
