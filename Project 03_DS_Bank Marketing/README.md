Task-03

Build a decision tree classifier to predict whether a customer will purchase a product or service based on their demographic and behavioral data. Use a dataset such as the Bank Marketing dataset from the UCI Machine Learning Repository.

# Step-by-Step Explanation
# 1. Load the Dataset
import pandas as pd
# Load the dataset
df = pd.read_csv(bankfull.csv)

# 2. Data Preprocessing
Prepare the data for modeling by handling missing values, encoding categorical variables, and splitting the data
into features and target variable.
1.Check for missing values
print(df.isnull().sum())
2.Encode categorical variables
df = pd.get_dummies(df, drop_first=True)
 Define features (X) and target (y)
X = df.drop('y_yes', axis=1)
y = df['y_yes']

# 3. Split the Data
Split the data into training and testing sets to evaluate the model’s performance.
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)
# 4. Build the Decision Tree Classifier
Use the DecisionTreeClassifier from scikit-learn to build the model.
from sklearn.tree import DecisionTreeClassifier
4.1 Initialize the classifier
clf = DecisionTreeClassifier(random_state=42)
4.2  Train the classifier
clf.fit(X_train, y_train)
# 5. Evaluate the Model
Evaluate the model’s performance using metrics such as accuracy, precision, recall, and the confusion matrix.
from sklearn.metrics import accuracy_score, precision_score, recall_score, confusion_matrix
5.1 Make predictions
y_pred = clf.predict(X_test)
5.2  Calculate metrics
accuracy = accuracy_score(y_test, y_pred)
precision = precision_score(y_test, y_pred)
recall = recall_score(y_test, y_pred)
conf_matrix = confusion_matrix(y_test, y_pred)
print(f'Accuracy: {accuracy}')
print(f'Precision: {precision}')
print(f'Recall: {recall}')
print(f'Confusion Matrix:\n{conf_matrix}')
# Summary
# 1. Load the Dataset: Download and load the dataset into a pandas DataFrame.
# 2. Data Preprocessing: Handle missing values, encode categorical variables, and define features and target
variable.
# 3. Split the Data: Split the data into training and testing sets.
# 4. Build the Model: Initialize and train the decision tree classifier.
# 5. Evaluate the Model: Use metrics like accuracy, precision, recall, and confusion matrix to evaluate the
model’s performance.
