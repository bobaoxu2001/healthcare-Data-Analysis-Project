# 🏥 Medical Cost Data Analysis - EDA

Today we will explore a data set dedicated to the cost of treatment of different patients. The cost of treatment depends on many factors: diagnosis, type of clinic, city of residence, age, and so on. We have no data on the diagnosis of patients. But we have other information that can help us make a conclusion about the health of patients and practice regression analysis.

In any case, I wish you to be healthy! Let's look at our data.

---

## 🔧 Steps

* Encode categorical features like gender, smoker, etc.
* Correlation between features on costs:


* Distribution of charges for smokers and non-smokers  
* Distribution of genders  
* Distribution of age  
* Distribution of age vs. charges (non-smokers)  
* Distribution of age vs. charges (smokers)  
* Distribution of BMI  
* Distribution of BMI vs. charges  
* Predict the cost of treatment  
  - **Linear Regression**: 0.796  
  - **Polynomial Features + Linear Regression**: 0.885  
  - **Random Forest Regressor**: 0.89  

---

## 📊 Visualization Analysis (Descriptive Summary)

### Correlation Matrix
A strong correlation is observed only with the patient's smoking status. Surprisingly, BMI shows only a modest correlation with charges.

### Charges for Smokers vs. Non-Smokers
Smoking patients tend to spend significantly more on treatment. However, the dataset contains more non-smokers, which may balance overall costs.

### Gender Distribution
- Females are encoded as `1`, males as `0`.  
- More male smokers than female smokers were observed.  
- Given smoking's influence, total treatment costs for men are likely higher.

### Age Distribution
Most patients are between 20 and 60 years old, with a fairly even spread within that range.

### Age vs. Charges
- For **non-smokers**, charges tend to increase gradually with age.
- For **smokers**, the increase in charges is more rapid and significant.

### BMI Distribution
- BMI values span a wide range, with 30 as the threshold for obesity.
- Obese patients (BMI > 30) generally face higher treatment costs.

### BMI vs. Charges
There is a weak to moderate positive relationship between BMI and charges, though not as strong as that of smoking.

### Model Results
Among the models tested:
- Linear regression performs reasonably well.
- Polynomial regression adds noticeable improvement.
- Random Forest provides the best performance with an R² score of **0.89**.

---

## ✅ Summary

- **Smoking** is the most influential feature affecting medical costs.
- **Age** and **BMI** follow, with more moderate effects.
- **Gender**, **region**, and **number of children** have minimal impact individually.
- Even simple regression models perform well given the strong influence of a few key variables.

---

*EDA conducted by **Ao Xu***  
*M.S. Data Science | New York University*

