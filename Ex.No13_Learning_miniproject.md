# Ex.No: 10 Learning – Use Supervised Learning  
### DATE: 06/05/2024
### REGISTER NUMBER : 212221060123

### AIM: 
To write a program to train the classifier for diabetes accuracy analysis model.
###  Algorithm:
Step 1- Collect a dataset with features and labels. 
Step 2- Data Preprocessing like handle missing values and split datas for feature scaling. 
Step 3- Choose a suitable machine learning model logistic regression 
Step 4- Train the selected model on the training dataset 
Step 5- Evaluate the trained model on the testing dataset 
Step 6- Optimize model hyperparameters to improve performance like random search or grid search. 
Step 7- Deploy the model for real world predictions.
### Program:
```
# prompt: diabetes model 
# Import necessary libraries
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Load the diabetes dataset
diabetes = pd.read_csv('diabetes.csv')

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(diabetes.drop('Outcome', axis=1), diabetes['Outcome'], test_size=0.25)

# Train the Logistic Regression model
model = LogisticRegression()
model.fit(X_train, y_train)

# Evaluate the model on the testing set
y_pred = model.predict(X_test)
accuracy = model.score(X_test, y_test)

# Print the accuracy of the model
print(f"Accuracy: {accuracy}")
```
### Output:
  Accuracy: 0.7395833333333334 

### Result:
Thus the system was trained successfully and the prediction was carried out.
