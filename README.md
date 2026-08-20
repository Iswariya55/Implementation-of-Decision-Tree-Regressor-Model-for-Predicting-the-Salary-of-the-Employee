# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries such as Pandas, train_test_split, DecisionTreeRegressor, and evaluation metrics.
2.Load the Employee dataset and preprocess the data by converting categorical features into numerical values.
3.Split the dataset into training and testing sets, then train the Decision Tree Regressor using the training data.
4.Predict the employee's salary using the trained model and evaluate the model's performance using an appropriate regression metric.

## Program:
```
import pandas as pd
from sklearn.tree import DecisionTreeRegressor
import matplotlib.pyplot as plt

# Load the dataset
data = pd.read_csv("Salary (1).csv")

# Display the dataset
print(data)

# Select input and output
X = data[["Level"]]
y = data["Salary"]

# Create Decision Tree Regressor
model = DecisionTreeRegressor(random_state=0)

# Train the model
model.fit(X, y)

# Predict salary for Level 6.5
new_data = pd.DataFrame([[6.5]], columns=["Level"])
prediction = model.predict(new_data)

print("\nPredicted Salary for Level 6.5:", prediction[0])

# Predict salaries for existing levels
y_pred = model.predict(X)

print("\nPredicted Salaries:")
print(y_pred)

# Plot
plt.scatter(X, y)
plt.plot(X, y_pred)
plt.xlabel("Level")
plt.ylabel("Salary")
plt.title("Decision Tree Regression - Salary Prediction")
plt.show()

/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Ishwarya R
RegisterNumber: 212224220039
*/
```

## Output:

<img width="831" height="408" alt="image" src="https://github.com/user-attachments/assets/83b8dd4c-fa78-4f89-bb04-57c1ae613a4a" />
<img width="860" height="622" alt="image" src="https://github.com/user-attachments/assets/0ec9243b-b7e4-4846-ba72-ef40d38ddb96" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
