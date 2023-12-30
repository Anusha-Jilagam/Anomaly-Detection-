## Automated Anomaly Detection for Predictive Maintenance

## Objective
We are provided with processing data from equipment to find Anomalies.

This Capstone project is aimed at predicting the machine breakdown by identifying the anomalies in the data.

## DESCRIPTION
Many different industries need predictive maintenance solutions to reduce risks and gain actionable insights through processing data from their equipment.
Although system failure is a very general issue that can occur in any machine, predicting the failure and taking steps to prevent such failure is most important for any machine or software application.
Predictive maintenance evaluates the condition of equipment by performing online monitoring. The goal is to perform maintenance before the equipment degrades or breaks down.
## Model Trainig and Evaluation Steps Involved:

### Started with importing basic necessary libraries.
- Libraries like pandas, numpy, matplotlib, seaborn.
- Imported remaining Libraries where ever required.
### Dataset Details
- Total number of rows in data: 18398
- Total number of columns: 62
### Descriptive Statistics
- Basic statistics from each column displayed using describe.
### Changing datatype for time column to DataTime.
- As the time time column is in string format changed it to Datatime.
### Null Values
- There are not null values in the data.
### Duplicate Values
- There are not duplicate values in the data.
### Plotting
- Plotted a time series plot to understand the data change over time period for random 2 columns as all columns are x values.
- Plotted a heatmap to see the data density.
### Feature Engineering
- Scaled the dataset with Satandard Scaler.
- Ordinally encoded time column.
### Finding Outliers and Treating Outliers
- Visually represented outliers in the dataset after scaling.
- Used zscore to find out rows with outliers.
- Treated outliers using zscores and exported cleaned data
- Again checked for outliers and treated X19 column.
### Checking if there is any imbalance
- Used countplot to understand distribution of data in output variable.
- The dataset is highly imbalanced.
### Splitting Dataset
- Splitted the data into train, validation and test data sets.
### Sampling Techinique on training dataset
- Performed under sampling using Random under Sampler on training dataset
### Model Selection
- As the output is classification between anomaly yes or no opted for Classification models as
- Logistic Regression
- Desicion Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- Support Vector Classifier
- KNeighbours Classifier
- XG Boosting Classifier
- Isolation Forest Classifier
### Training and Testing
- Trained the undersample data with all above mentioned models.
- Made predictions with validation data to test the models.
### Evaluation 
- Checked Accuracy Score, ROC AUC Score and Classification Report for all models.
### Best Model Evaluation
- Using a for loop found best model with minimun threshold of 0.75 and maximum threshold of 0.99.
- Isolation Forest Classifiers Turned out to BEST MODEL with Accuracy of 0.96.
### Hyperparameter Tuning
- Performed Hyperparameter Tuning using GridSearch CV
- Best estimator from Grid Search CV achieved an accuracy of 0.90.
### Final Prediction On Test Data
- Done Prediction of Anomalies on test data.
- Achieved an accuracy of 0.90 on test data


## Difficulties Faced
- As there are two y columns it was difficult to handle the training.
  - Decided to drop one column and  made decision by checking two variables and opted for less imbalanced one.
- Finding Outliers as there is a large set of columns
  - Tried displaying all columns in boxplot for finding outliers.
- Understanding Data
  - As the data is all numerical is was a bit hard to understand the data distribution.

# Conclusion
- Even though Isolation Forest Performed best on traiing and validation data if could perform well on Test data and predict anomalies. Random forest performed well with test data set and achieved an accuracy of 90%.
