

````markdown
 Train-Test Split Demonstration with Car Price Dataset

This project demonstrates how to split a car price dataset into training and testing sets using scikit-learn’s train_test_split() method.
The dataset includes key features such as mileage, age, and selling price, forming the foundation for building predictive machine learning models


 📁 Dataset

File: `carprices.csv`  
The dataset contains the following columns:

- 🚗 `Mileage`: The total distance the car has traveled (in km)
- ⏳ `Age(yrs)`: Age of the car in years
- 💰 `Sell Price($)`: The selling price of the car (target variable)



 🧪 Steps Performed

 1️⃣ Import Required Libraries

```python
import pandas as pd
from sklearn.model_selection import train_test_split
````



### 2️⃣ Load the Dataset

```python
df = pd.read_csv("carprices.csv")
```



### 3️⃣ Feature & Target Separation

```python
# Input Features
X = df[['Mileage', 'Age(yrs)']]

# Target Variable
y = df[['Sell Price($)']]
```

* ✅ `X` contains the features used to predict the car price.
* 🎯 `y` is the label we are trying to predict.



### 4️⃣ Split into Training and Testing Data

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=3
)
```

* 📌 `test_size=0.2`: Reserves 20% of the data for testing.
* 🔒 `random_state=3`: Ensures the split is reproducible on every run.

---

## 🎯 Purpose

* ✅ To **prepare data** for training a machine learning model.
* 🚫 To **avoid overfitting** by evaluating model performance on unseen (test) data.
* 🧪 A critical step in any supervised learning pipeline.



## 🛠️ Requirements

Make sure you have the following installed:

* Python 3.x
* pandas
* scikit-learn

Install using pip:

```bash
pip install pandas scikit-learn
```




