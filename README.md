# Vehicle-Fraudulent-Claims-Capstone
![image](https://user-images.githubusercontent.com/95660642/192659637-5908361d-8485-464f-a82e-7fd8083a46cc.png)
### Introduction
Vehicle Insurance Fraud is a major area of losses to the auto insurance companies. Study conducted by
Verisk, indicated that insurance companies had to bear losses to the tune of $29 billion a year [1](https://www.iii.org/article/background-on-insurance-fraud).
According to Progressive, auto insurance fraud is committed when someone falsely claims about an event
and get monetarily compensated[2](https://www.progressive.com/answers/car-insurance-fraud). In this project an attempt has been made to explore major
contributing factors which have led to fraud along with developing models which can distinguish
fraudulent transactions. For this model data is obtained from [Vehicle Insurance Claim Fraud Detection](https://www.kaggle.com/shivamb/vehicle-claim-fraud-detection)

### Problem statement
How can Data Science be leveraged to detect Vehicle Insurance Fraudulent claims to reduce losses on 
account of exaggerated and false claims about accidents, property damage and physical injury by 
developing machine learning models which can improve the accuracy as measured by F1 SCORE to 
above 0.8 in 6 months

### Data Wrangling & Exploratory Data Analysis
[Data Wrangling and Exploratory Data Analysis NoteBook](https://github.com/vishrast/Vehicle-Fraudulent-Claims-Capstone/blob/ad45778b23be1dffabdd59e085c499ec3469dfd2/Data%20Wrangling%20and%20Exploratory%20Data%20Analysis.ipynb)

During this phase we cleaned the data and gained insights about the data set.
![image](https://user-images.githubusercontent.com/95660642/192667584-6cf51c47-74ee-4581-a4a2-3f7c119f6868.png)
![image](https://user-images.githubusercontent.com/95660642/192667765-333a3d53-27b7-49d8-be20-46e542b8f44f.png)

The address change in last 6 months,Utility vehicle had higher probablity of of fraudulent claims. Impact of other features on fraudulent transactions can be seen in the note book attached above

### Pre-Processing, Training and Modeling
The pre-processing, training and modeling steps are including in the notebooks attached below
[Pre-processing & Training-1](https://github.com/vishrast/Vehicle-Insurance-Fraud-Detection-/blob/1f88b674e4e48d3f1f7d527ea05480f6dfe99205/Pre-Processing%20and%20Training-%20Phase%201.ipynb)
[Pre-processing & Training-2](https://github.com/vishrast/Vehicle-Insurance-Fraud-Detection-/blob/1f88b674e4e48d3f1f7d527ea05480f6dfe99205/Pre-Processing%20and%20Training-Phase2.ipynb)
[Modeling](https://github.com/vishrast/Vehicle-Insurance-Fraud-Detection-/blob/1f88b674e4e48d3f1f7d527ea05480f6dfe99205/Modeling.ipynb)
The key metrics of importance for fraud detection predicition model is choosed as F1 score, which is the harmonic mean of precision and recall. The biggest constaint for this data set is its imbalanced nature with 94.1% of transactions being  non-fraudulent. Additionally majority of features were categorical making generalization of the model difficult. Finally, SMOTEN for class balancing, Weight of Evidence Encoder for categorical encoding, and logistic regression model with class weight optimization were used for final model selection and f1 score imroved to 0.85

![image](https://user-images.githubusercontent.com/95660642/192673052-0d9acbd6-2583-4de4-b5bd-58230c812982.png)

![image](https://user-images.githubusercontent.com/95660642/192673127-143e45d6-66ae-49ad-90a8-9db2b455414c.png)

![image](https://user-images.githubusercontent.com/95660642/192673177-8743dc1b-ec81-4360-abd9-3ee1a33ceca5.png)


### Key Findings
•	SMOTEN balancing combined with weight of evidence encoder, and tuned Logistic Regression model with class weight optimization, gave the best results and F1 score of 0.85 is achieved on minority class on validation data.

•	Dummy encoding approach did not generalize well due to too many features

•	Logistic regression with optimized class weight without balancing, generalized well but F1 score was only 0.22

•	Utility vehicles have higher probability of fraudulent claims in vehicle categories

•	Higher probability of fraud if address is changed within last 6 months 

•	Higher end vehicles like Mercedes, BMW and Acura are more involved in fraudulent claims

•	Decision making threshold can be moved based on the business needs

### Further Work
The data set had several limitations as the data set only consisted of categorical variables and was highly imbalanced. Most of the models failed due to that. There are several other techniques to deal with categorical data [https://contrib.scikit-learn.org/category_encoders/](https://contrib.scikit-learn.org/category_encoders/ and imbalanced target variable https://imbalanced-learn.org/stable/), which were not tried out and can be tried out to see if model performance can be improved further





