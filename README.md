# 🏥 Medical Cost Data Analysis - EDA

Today we will explore a data set dedicated to the cost of treatment of different patients. The cost of treatment depends on many factors: diagnosis, type of clinic, city of residence, age and so on. We have no data on the diagnosis of patients. But we have other information that can help us to make a conclusion about the health of patients and practice regression analysis.

In any case, I wish you to be healthy! Let's look at our data.

---

## 🔧 Steps

* Encode categorical features like gender, smoker, etc.
* Correlation between features on costs:

region -0.006208
sex 0.057292
children 0.067998
bmi 0.198341
age 0.299008
smoker 0.787251
charges 1.000000


* Distribution of charges for smokers and non-smokers  
* Distribution of genders  
* Distribution of Age  
* Distribution of Age VS Charges (non-smokers)  
* Distribution of Age VS Charges (smokers)  
* Distribution of BMI  
* Distribution of BMI and Charges  
* Predict the cost of treatment  
  - **Linear Regression**: 0.7962732059725784  
  - **PolynomialFeatures + Linear Regression**: 0.8849197344147238  
  - **RandomForestRegressor**: 0.89  

---

## 📊 Visualization Analysis

![Image 1](Correlation_Matrix.png)  
*A strong correlation is observed only with the fact of smoking the patient. To be honest, I expected a higher correlation with BMI. Well. We investigate smoking in more detail.*

![Image 2](Distribution_of_charges_for_smokers_non_smokers.png)  
*Smoking patients spend more on treatment. But there is a feeling that the number of non-smoking patients is greater.*

![Image 3](Distribution_of_genders.png)  
*Note that women are coded with the symbol "1" and men - "0".*

Also we can notice that more male smokers than women smokers. It can be assumed that the total cost of treatment in men will be more than in women, given the impact of smoking.

![Image 4](Distribution_of_Age.png)  
*Most of the patients are between 20 to 60 years old.*

![Image 5](number_of_smokers_and_non_smokers.png)  
*The number of smokers and non-smokers (18 years old).*

![Image 6](Distribution_of_charges_and_age_for_non_smokers.png)  
*Distribution of charges and age for non-smokers.*

![Image 7](Distribution_of_charges_and_age_for_smokers.png)  
*Distribution of charges and age for smokers.*

![Image 8](Distribution_of_BMI.png)  
*Distribution of BMI.*

With a value equal to 30 starts obesity. Let's look at the distribution of costs in patients with BMI greater than 30 and less than 30.

![Image 9](Distribution_of_charges_for_patients_with_critical_BMI.png)  
*Distribution of costs in patients with BMI greater than 30 and less than 30.*

![Image 10](Distribution_of_and_Chargesnad_BMI.png)  
*Distribution of BMI and Charges.*

![Image 11](model_results.png)  
*Model Results.*

---

## ✅ Conclusion

- Smoking has the strongest correlation with medical charges.
- Age and BMI have moderate influence.
- Other features such as sex, region, and number of children have little impact.
- Random Forest performed best among models with an R² score of 0.89.

---

*Analysis conducted by **Ao Xu***  
*M.S. in Data Science | New York University*
