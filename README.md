[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1H4g1oZW2J2e7JxfeHcOVBdH-HCm7WIVF)





# Learning Analytics & Educational Data Mining
Student performance is often used to assess quality of education. often, the metrics used to measure and/or predict student performance are the Cumulative Grade Point Average (CGPA) and internal assessments. Some researches in the past have expanded the scope of metrics to include other aspects about the students such as amount of time spent studying, distane travelled to get to school, family relations, free time they get and internet access. Others have, on a larger scope, studied how students rated the structure and delivery of course content by instructors as this plays a big role in their perfromance.This project attempts to improve educationl systems using the above-mentioned data. the project will make use of data science principles and machine learning models to identify attributes that have the most correlation to student perfromance and predict future performance based on these.

## The project seeks to answer the following questions:

    1. What are the factors affecting student achievements?
    2. Can the factors above be used to predict student scores?
   
## Data Sets:
    
    1. Student Performance Data Set

**After Analysis:**

 We have established some student attributes such as previous grades have a positive linear correlation to their final grade. Others such as weekday alcohol consumption, abscences and romantica relationships have a negative correlation to their final grade. Also being in certain categories of gender, rural/urban areas or schools may increase the odds of performing better. Some attributes have no clear pattern in correlation. Some of the most interesting insights that we've found from the data are:
- Weekend alchol consumption has less detrimentl effects to performance than weekday alcohol consumption.
- Students who perform poorly do not wish to get higher education.
- Students whose parents are teachers have the lowest median\average, while those whose parents are in health proffessions perform better.
- Students with very bad family relations perfom better than those with better family relations.
- students with access to internet have better average scores.

Since decision tree was one of the best performing models, We used the decision tree classifier to plot the decision tree, so as to identify the most significant attributes that were used in predicting the target variable:
    
As expected, the first grade 'G2' being the root node is the most significant attribute. The top ones spotted are:
- G2
- Abscences
- family relations
- G1
- Study time
- travel time
- How often a student goes out
- reason for joining their school
- How much students engage with activities outside class
- guardian

These are student attributes that play a significant role in what a student scores and hence can be used to predict their future scores. The best method achieved for predicting these scores is the XGBoost classifier (@ 87.788%). This was made possible through the following steps:
1. Encoding of string variables
2. Mapping of all grades to just 5 categories
3. Feature selection through Boruta
4. Parameter Tuning using grid search method