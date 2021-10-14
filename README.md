# CapstoneProject
# Analyzing Risk Factors Associated  with Obesity/Overweight Using Machine Learning

## Contributors:<br/>
Siyu Ma<br/>
Sandra Pinto<br/>
Shruthi Boban<br/>

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
Approach: Both classification and Regression models including K-Nearest neighbor, Classification and Regression Tree, support Vector Machine, Multi-Layer Perceptron, Ada boosting with decision tree, Gradient Boosting, Random Forest, LASSO (Least Absolute Shrinkage and Selection Operator), and Elastic Regression. <br/>
Findings: Using affect-related variables it is possible to predict the BMI with a good level of accuracy and the psychological variable that had most impact on the predictive capabilities of the algorithms is Depression
The best performance was achieved by the LASSO and Elastic Net, with a MAE (mean absolute error) equal to 4.35 and the PCCs (Pearson correlation coefficient ) respectively of 0.81 and 0.80, indicating a strong correlation between predictions and real value.<br/>
Limitations:Restricted number of subjects<br/>
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
#### Box plot of BMI Distribution by Age Groups:<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Age%20Groups(All%20ages).png)
- Since the visualizations showed that the age group of 20-60 contains the majority of the data, and education, income ratio, mental health, and other factors showed more resonable relation for adults. We decided focus on respondent from 20-60, and expand the project to childhood obesity/overweight and senior(60+) obesity/overweight in future studies.
#### Box plot of BMI Distibution by Age Groups(20-60):<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Age%2020-60.png)
- The box plot shows that adults in age range from 30-60 have higher BMI compared to adults in 20-29 age group. Adults in 40-49 have higher BMI compared to adults in 30-39 age group based on the median and upper quantiles.

#### Box plot of Adult BMI and Gender:<br/> 
- The overall adults female BMI is higher than adults male BMI in our dataset. The median of adult female BMI is slightly higher than the median of adult male BMI, however, the overall range of adult female BMI is greater based on the plot. <br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Gender(Adults).png)

#### Box plot of Adult BMI and Race:<br/> 
- We noticed that None-Hispanic Asians Adults have significantly lower BMI compared to other races.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Race(Adults).png)

#### Box plot of Adult BMI and Education level:<br/> 
- Adults with college degree or above tend to have lower BMI compared to adults with other education levels.<br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Education%20level(Adults.).png)

#### Bar chart of Adult BMI and Depression:<br/> 
- Respondents with depression related experiences tend to have higher BMI compared to others. Adults claimed depressed or feel down for "More than half the days" shows higher BMI. <br/>
![alt text](https://github.com/DATA606Project-TeamS/CapstoneProject-ObesityandML/blob/main/Output/BMI%20and%20Depression(Adults).png)



## Datasets Used
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Demographics&Cycle=2017-2020
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Examination&Cycle=2017-2020
- https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Questionnaire&Cycle=2017-2020
## References
- Chatterjee A, Gerdes MW, Martinez SG. Identification of Risk Factors Associated with Obesity and Overweight—A Machine Learning Overview. Sensors. 2020; 20(9):2734. https://doi.org/10.3390/s20092734 
- Wilfley, D. E., Hayes, J. F., Balantekin, K. N., Van Buren, D. J., & Epstein, L. H. (2018). Behavioral interventions for obesity in children and adults: Evidence base, novel approaches, and translation into practice. American Psychologist, 73(8), 981–993. https://doi-org.proxy-bc.researchport.umd.edu/10.1037/amp0000293
- CDC. (2021, March 1). Why It Matters. Centers for Disease Control and Prevention. https://www.cdc.gov/obesity/about-obesity/why-it-matters.html Centers for Disease Control and Prevention. (2021, August 27). About adult BMI. Centers for Disease Control and Prevention.   
- Retrieved September 29, 2021, from https://www.cdc.gov/healthyweight/assessing/bmi/adult_bmi/index.html. 
- Ferdowsy, F.,Rahi, K. S. A., Jabiullah, Md. I., Habib, Md. T. (2021, August 5). A Machine Learning approach for obesity risk prediction. Current Research in Behavioral Science, 2, 2021. https://doi.org/10.1016/j.crbeha.2021.100053 
- Delnevo, G., Mancini, G., Roccetti, M., Salomoni, P., Trombini, E., & Andrei, F. (2021). The Prediction of Body Mass Index from Negative Affectivity through Machine Learning: A Confirmatory Study. Sensors, 21(7). https://doi.org/10.3390/s21072361
- Pillai , R., Saravanan, S., &amp; Shyam, D. G. K. (2020, December 8). The BMI and mental Illness NEXUS: A machine learning approach. IEEE Xplore. Retrieved September 29, 2021, from https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&amp;arnumber=9277446.
