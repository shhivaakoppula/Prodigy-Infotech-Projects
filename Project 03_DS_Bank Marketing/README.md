

 # Task-03 : Build a decision tree classifier to predict whether a customer will purchase a product or service based on their demographic and behavioral data. Use a dataset such as the Bank Marketing dataset from the UCI Machine Learning Repository.

# Explanation
1.Import Libraries : We import libraries for data manipulation (pandas, numpy), model building (scikit-learn), and visualization (matplotlib, seaborn).
2.Load the Dataset : We load the dataset from the UCI repository into a pandas DataFrame.
3.Data Preprocessing:
3.1 Encode Categorical Variables : Convert categorical variables into numerical format using one-hot encoding.
3.2 Split the Data into Features and Target : Separate the features (X) from the target variable (y).
3.3 Split the Data into Training and Testing Sets : Split the data into training and testing sets to evaluate the model’s performance.
4.Train the Classifier:
4.1 Initialize the Classifier: Create an instance of the decision tree classifier.
4.2 Train the Classifier: Fit the classifier to the training data.
5. Evaluate the Model:
5.1 Make Predictions: Use the trained model to make predictions on the test data.
5.2 Calculate Accuracy: Measure the accuracy of the model.
Print Classification Report: Get detailed metrics like precision, recall, and F1-score.
Print Confusion Matrix: Visualize the confusion matrix to understand the model’s performance.
