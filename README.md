## Employee Statistics

The dataset stores the employee attributes with some earning more than 50K while others less than 50K annually. Attributes of the employee known to us are as follows: 

<ul>
<li><b>age:</b> Age of the employee</li>
<li><b>workclass:</b> Workclass of the employee</li>
<li><b>education:</b> Highest qualification of the employee</li>
<li><b>education-num:</b> Total number of years spent in education</li>
<li><b>marital-status:</b> Marital Status of the employee</li>
<li><b>occupation:</b> Profession of the employee</li>
<li><b>relationship:</b> Dependents of the employee</li>
<li><b>race:</b> Ethnicity of the employee</li>
<li><b>sex:</b> Gender of the employee</li>
<li><b>hours-per-week:</b> Hours per week of the employee</li>
<li><b>native-country:</b> Native country of the employee</li>
<li><b>hours-per-week:</b> Salary: 50K or more</li>
</ul>

The classes are categorized into two types: "Yes" and "No" and not balanced (e.g. there are many more "No" than "Yes"). No missing values were found. Outliers are detected and removed. Additionally, we are using feature scaling techniques.

## Goal

The objective is to classify the data using binomial classification. A list of machine learning models will be trained and tested to determine which will yield the best results:

- Logistic Regression
- MLP Classifier
- Random Forest Classifier
- AdaBoost Classifier

## Exploratory Data Analysis

![age_sex_count](https://github.com/rodrickmascarenhas/employee-statistics/assets/30309234/e61d7a77-1f04-46c1-8d69-d32f91fe4f65)


As the age increases, so does the salary of the employee. We don't see employees earning more than 50K in their early 20s

![sex_workclass_distribution](https://github.com/rodrickmascarenhas/employee-statistics/assets/30309234/aedacb07-ea0e-40a0-af8f-002e152a7a3a)


Capacity comprises of more than 30% of the workforce are Female.
Employees belonging to Private companies are much more than those of other workclasses

![hours_per_week_for_occupation](https://github.com/rodrickmascarenhas/employee-statistics/assets/30309234/a8c71dd4-3ca4-48df-abd5-f02811b4079f)


In most occupations, employees work 40 hours a week except Armed Forces
Employees working as 'Exec-managerial' or 'Prof-specialty' require more expertise and therefore earn more than others

## Results

Best Model: MLP Classifier
Best Score: 0.792

![confusion_matrix](https://github.com/rodrickmascarenhas/employee-statistics/assets/30309234/0ef9b02f-c67f-4ad4-8985-a5c9bb842dbe)


We can predict whether an employee will have a salary > 50K by the recall. If precision determines the accuracy of our model, then recall evaluates the model's ability to serve the purpose intended. It appears our model can correctly predict the outcomes up to 53%.
Type 1 errors are observed as assuming Salary_50K is "Yes" when actually that is false. Type 2 errors are observed as assuming Salary_50K is "No" when actually that is not true

![roc_curve](https://github.com/rodrickmascarenhas/employee-statistics/assets/30309234/4c9859e2-3096-4b2e-bc04-93dcd61add45)


A ROC curve of 0.69 is moderate level of accuracy in distinguishing between positive and negative classes. Classifiers that give curves closer to the top-left corner indicate a better performance of the model.
