
## Heart Attack Analysis And Prediction.

The Aim of this project is to classify whether a patient is at a risk of heary attack or not.

What is a heart attack?

![heart attack](https://user-images.githubusercontent.com/95433685/180605233-e3caef13-9136-478e-9725-11b69b888b88.png)

* A myocardial infarction (commonly called a heart attack) is an extremely dangerous condition caused by a lack of blood flow to your heart muscle.
* A heart attack (myocardial infarction) happens when one or more areas of the heart muscle don't get enough oxygen. This happens when blood flow to the heart muscle is blocked.

How Does a Heart Attack Occur?

![heart-attack-causes-722x406 (1)](https://user-images.githubusercontent.com/95433685/180605275-24f4c7c1-080a-4b16-a119-a936cf2dc10f.jpg)

* A heart attack occurs when an artery that sends blood and oxygen to the heart is blocked.

What are the symptoms of Heart attack?

![Heart-Attack-Signs-Men-Women](https://user-images.githubusercontent.com/95433685/180605307-57ce80da-cbe2-41e9-a1fd-18350a31270d.jpg)

## Variables in the dataset 

1. age - age in years


2. sex - sex (1 = male; 0 = female)


3. cp - chest pain type (1 = typical angina; 2 = atypical angina; 3 = non-anginal pain; 0 = asymptomatic)


4. trtbps - resting blood pressure (in mm Hg on admission to the hospital)


5. chol - serum cholestoral in mg/dl


6. fbs - fasting blood sugar > 120 mg/dl (1 = true; 0 = false)


7. restecg - resting electrocardiographic results (1 = normal; 2 = having ST-T wave abnormality; 0 = hypertrophy)


8. thalach - maximum heart rate achieved


9. exang - exercise induced angina (1 = yes; 0 = no)


10. oldpeak - ST depression induced by exercise relative to rest


11. slope - the slope of the peak exercise ST segment (2 = upsloping; 1 = flat; 0 = downsloping)


12. ca - number of major vessels (0-3) colored by flourosopy


13. thal - 2 = normal; 1 = fixed defect; 3 = reversable defect


14. num - the predicted attribute - diagnosis of heart disease (angiographic disease status)(Value 0 = < diameter narrowing; 
Value 1 = > 50% diameter narrowing)
## Initial Ananlysis on Dataset

* The dataset contains of 303 rows and 14 columns.
* The type of variables in the dataset are all numerical(int or float).
* The dataset does not contain missing values.
## Exploratory Data analysis 

* Determining variables with high unique values as numeric and with low unique values as categorical.

* Numerical variables: age, trtbps, chol, thalachh, oldpeak.

* Categorical variables: sex, cp, fbs, restecg, exng, slp, caa, thall, output.

## Analysis from the Distribution of Numerical vairables. 

Age Variable:

The vast majority of patients are between 50 and 60.
There is a remarkable place on the chart. There is a decrease in patients between the ages of 47-and 50.
It looks like there are no outliers in the variable.

Trtbps Variable:

The resting blood pressure of most patients is generally between 110 and 140.
Values after 180 can be considered as outliers.
There is a high patient traffic between 115-120, 125-130, and 155-160 values.

Cholesterol Variable:

Cholesterol value in most patients is between 200-and 280.
Values after 380 can be considered as outliers.

Thalach Variable:

The maximum heart rate achieved in most patients is between 145 and 170.
In particular, The values before 80 can be considered outliers.

Oldpeak Variable:

Values of the vast majority of patients in the variable range from 0 to 1.6.
Especially values after 4 can be considered as outliers.

## Analysis on Categorical variables:

Sex Variable

* 68.3% of the patients are male, 31.7% are female.
* So, the number of male patients is more than twice that of female patients.

Cp Variable

* Almost half of the patients have an observation value of 0. In other words, there is asymptomatic angina
Half of the patients are asymptomatic; they have pain without any symptoms.
* If we examine the other half of the pie chart, 1 out of 4 patients has an observation value of 2.
* In other words, atypical angina is in 29% of the patients.
* This observation value shows patients with shortness of breath or non-classical pain.
* The other two observation values are less than the others.
* 16.5% of patients have a value of 1. In other words, typical angina is seen. Typical angina is the classic exertion pain that comes during any physical activity.

Fbs Variable

* The vast majority of patients have an observation value of 0. In other words, 85%.
* The fasting blood sugar of these patients is less than 120 mg/dl.
* The remaining 15 percent have a more than 120 mg/dl fasting blood glucose level.

Rest_ecg Variable

* The thing that draws attention to the image of this variable is that the number of patients with two observation values is negligible.
* It has a value of 1.3 percent. When we look at all of these patients, it is not a very important number.
* This value represents the ST and T wavelengths of the patients.
* The size of those with 1, that is, the blue part on the graph is 50.2%
* The percentage of patients with a value of 0 is 48.5%.
* That is, the patients' values of 48.5% are hypertrophy.

Exang Variable

* We have said that this variable stands for exercise-induced angina.
* Angina is a type of chest pain caused by reduced blood flow to the heart.
* According to the variable "exang," the pain caused by this angina is represented by a value of 1 if it occurs with any exercise and 0 if it does not.
* In this context, Values 0 are more than twice as values 1. More than half of the patients do not have exercise-induced angina.

Slope Variable

* The minimum observation value is 0 with 7 percent.
* This is patients with a downward slope of the ST wavelength.
* The other two observation values are almost equal to each other.
* The ST wavelength of half of the remaining patients is 1, that is straight, while the observation value of the other half is 2, that is, the ST wavelength is sloped upwards.

Ca variable

* This variable is the number of great vessels colored by fluoroscopy.
* In more than half of the patients, 57.8 percent, the number of large vessels is 0. That is, the number of large vessels colored by fluoroscopy is absent.
* After 0 observation value, the other value with the most slices in the pie chart is 1.
* The number of large vessels observed in 21.5% of the patients is 1

Thal Variable

* The "Thal" variable is short for the "Thallium stress test."
* The thallium stress test is simply an imaging method that evaluates the amount of blood reaching the heart muscle and determines whether a person has coronary artery disease.
* In this context, according to the thallium stress test results, 54.8 percent of the patients do not have coronary heart disease. The test results are Normal
* 36.8 percent has a value of 3, so we can say that this value is a reversible defect as an explanation.
* 5.9 percent of patients have a value of 1, so the test result for these patients is a fixed defect.

Target Variable

* More than half of the patients, 54.5 percent, have a heart attack risk. The remaining 45.5 percent have no heart attack risk

## Heatmap For Determing Corelation: 
![Heatmap](https://user-images.githubusercontent.com/95433685/180605858-9eab982a-94a9-4ab7-a4bc-7e3309b4f198.png)

Analysis from corelation Heatmap: 

Age Variable
* The variable thallach has negative moderate corelation  with the age variable.
* The severity of the correlation is -0.40. In other words, there is an inverse relationship between the "age" and "thalach" variables.
* We can say that the amount of heart rate reached decreases as age increases because there is an inverse proportion between them.


Trtbps Variable
* The variable with the highest correlation with the "trtbps" variable is the "age" variable. The correlation between them is 0.28.
* There is a positive low-intensity correlation.

Chol Variable
* The variable with the highest correlation with the "chol" variable is the "age" variable
* There is a correlation with a magnitude of 0.21. This is a low positive correlation.
* So, we can say that as age increases, cholesterol also increases.

Thalach Variable
* The variable with the highest correlation to the "Thalach" variable is the "target" variable.
* There is a 0.42 positive and moderate correlation between them. In other words, it is a variable that can directly trigger a heart attack.

Oldpeak Variable
* The correlation is -0.58 with the "slope" variable.
* There is a negative correlation between them, which is slightly above medium intensity.


Sex Variable
* There is no proper correlation between the variable "Sex" and other variables.
* The highest figure is -0.28 with the target variable. There is a negative low-intensity correlation between them.


Cp Variable
* Cp variable captures the high correlation with "thalach", "exang", and "target" variables.
* The highest is again the "target" variable.

Fbs Variable
* The "Fbs" variable does not correlate with other variables.
* The highest correlation with 0.18 belongs to the "trtbps" variable. There is a low positive correlation.


Rest_ecg Variable
* There is no strong correlation between the "Rest_ecg" variable and other variables.
* The highest correlation was 0.14 with the "target" variable. There is a positive low-intensity correlation.


Exang Variable
* The variable with the highest correlation to the exercise-induced angina variable is the target variable with -0.44

Slope Variable
* The variable with the highest correlation to the "slope" variable is the old peak variable. 
* There is an above-moderate correlation between these two. It is the most significant relationship in the table with 0.58


Ca Variable
* The variable with which the "Ca" variable has the highest correlation is the target variable with -0.39.
* Then comes the "age" variable with 0.28. We can say that there is a low positive correlation with the age variable.


Thal Variable
* The variable with which the "Thal" variable has the highest correlation is the variable "target" with -0.36.
* It has not had very high correlation coefficients with other variables.
## Model Preparation.

* Dropping Features With Low Corelation.

* Outlier detection and removal With Boxplot.
 
* Calculating IQR, Lower and Upper bridge for outlier removal.

* One hot Encoding on Categorical Varicables.

* Feature Scaling With RobustScaler method 

* Splitting the data in train and test.

* Used logistics regression algorithm for building classification model.

* The trained model got the accuracy of 88% with cross_validation score of 85%.


