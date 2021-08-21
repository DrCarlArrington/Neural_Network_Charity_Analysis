# Module 03 Challenge - Neural Network Charity Analysis
Researcher: Dr. Carl Arrington, Jr.

# Overview
The researcher used knowledge of machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup using the features in the charity_data.csv file.

The CSV contained more than 34,000 organizations that have received funding from Alphabet Soup over the years. The dataset contained a number of columns that captured metadata about each organization.

# Data Preprocessing
1. What variable(s) are considered the target for your model? - The "Is_Successful" column denotes whether the organization was successful if funded by Alphabet Soup.
2. What variable(s) are considered to be the features for your model? - NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
3. What variable(s) are neither and should be removed from the input data? EIN - (Employer Identification) and in the first two deliverables NAME was dropped as well as to not confuse the ML models into confusing significance
# Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and and activation functions did you select for your neural network model, and why? - In the optimization model there were three hidden layers each with many neurons, because this seeemed to increased the accuracy above 75%. The number of epochs wasn't changed. The first activation function was 'relu' but the 2nd and 3rd were 'sigmoid'and the output function was 'sigmoid'. Changing the 2nd and 3rd activation functions to 'sigmoid' also helped boost the accuracy.
5. Were you able to achieve the target model performance? - The target model performance was acheived.
6. What steps did you take to try and increase model performance? - The NAME column was converted into data points, which had the biggest impact on improving efficiency. The model also required adding a third layer and using the "sigmoid" activation function for the 2nd and 3rd layer.

# Summary
Tweaking the model to increase the accuracy above 75% allowed for the model to be able to correctly classify each of the points in the test data 75% of the time. Applicants for funding have nearly an 80% chance of being successful if they have the following:

* The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
* The type of APPLICATION is one of the following; T3, T4, T5, T6, T7, T8, T10, and T19
* The application has the following CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100.

A good model to recommend as an alternative is the Random Forest model because Random Forests are good for classification problems. Using this model produces a 77.6% accuracy for classifying data.
