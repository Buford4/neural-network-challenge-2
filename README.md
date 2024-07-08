# Project Report: Neural Network Challenge 2

## Background

The goal of this project was to create a neural network model to assist HR in predicting two key aspects:
1. Employee attrition (whether an employee is likely to leave the company).
2. The most suitable department for each employee.

A branched neural network was implemented to make these predictions concurrently.

## Repository Setup

1. Created a new repository named `neural-network-challenge-2`.
2. Cloned the repository locally.
3. Added the starter file `attrition.ipynb` to the local repository.
4. Pushed initial changes to GitHub.
5. Uploaded `attrition.ipynb` to Google Colab for development.
6. Periodically downloaded and pushed changes to ensure version control.

## Preprocessing

### Data Import and Exploration

1. **Data Import**: Imported the dataset and displayed the first five rows to get an initial view.
2. **Unique Values**: Determined the number of unique values in each column.

### Target and Features Preparation

3. **Target Variables**: Created `y_df` containing the `attrition` and `department` columns.
4. **Feature Selection**: Selected at least 10 columns (excluding `attrition` and `department`) to create `X_df`.

### Data Transformation

5. **Data Types**: Displayed the data types for `X_df`.
6. **Data Splitting**: Split the data into training and testing sets.
7. **Numeric Conversion**: Converted `X` data to numeric data types using appropriate encoders.
8. **Scaling**: Created a `StandardScaler`, fit it to the training data, and transformed both training and testing data.
9. **Encoding Targets**: 
   - Created a `OneHotEncoder` for the `department` column, fit it to the training data, and transformed both training and testing data.
   - Created a `OneHotEncoder` for the `attrition` column, fit it to the training data, and transformed both training and testing data.

## Model Creation, Compilation, and Training

### Model Architecture

1. **Input Layer**: Determined the number of columns in the `X` training data and created the input layer.
2. **Shared Layers**: Created at least two shared hidden layers.
3. **Branched Output Layers**:
   - Created a branch for predicting the `department` target column with one hidden layer and one output layer.
   - Created a branch for predicting the `attrition` target column with one hidden layer and one output layer.

### Model Compilation and Training

4. **Model Compilation**: Compiled the model with appropriate loss functions and optimizers.
5. **Model Summary**: Summarized the model to review its architecture.
6. **Model Training**: Trained the model using the preprocessed data.
7. **Model Evaluation**: Evaluated the model with the testing data and printed the accuracy for both `department` and `attrition` predictions.

## Summary and Insights

### Evaluation Metrics

- **Is accuracy the best metric?**: While accuracy is useful, other metrics like precision, recall, and F1 score could provide more insight, especially if the classes are imbalanced.
- **Activation Functions**: Chose `softmax` for the `department` output layer (to handle multi-class classification) and `sigmoid` for the `attrition` output layer (for binary classification).
- **Model Improvements**: Potential improvements include hyperparameter tuning, adding more layers, experimenting with different activation functions, and incorporating cross-validation for better model validation.

## Conclusion

This project successfully implemented a branched neural network model to predict employee attrition and the most suitable department. The preprocessing steps ensured the data was clean and appropriately formatted, and the model's architecture was designed to handle both predictions effectively. Further improvements and experimentation can enhance the model's performance and robustness.