# Rain Prediction Using Machine Learning

This project aims to predict whether it will rain the next day in Australia by analyzing a dataset containing about 10 years of daily weather observations from various locations across the country. The dataset is extensive, with 23 attributes including the target variable "RainTomorrow," which indicates whether it will rain the next day.

## Table of Contents
- [Importing Libraries](#importing-libraries)
- [Loading Data](#loading-data)
- [Data Visualization and Cleaning](#data-visualization-and-cleaning)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Conclusion](#conclusion)
- [End](#end)

## Importing Libraries

The libraries used in this project include:

- `numpy` and `pandas` for data manipulation,
- `matplotlib.pyplot` and `seaborn` for data visualization,
- `sklearn` for data preprocessing and model evaluation,
- `keras` for building the neural network model.

## Loading Data

The dataset was loaded from a CSV file, `weatherAUS.csv`, containing daily weather observations. The initial exploration showed various numeric and categorical attributes, with some missing values.

## Data Visualization and Cleaning

### Visualization:
- A count plot of the target column "RainTomorrow" showed data imbalance.
- A correlation heatmap helped identify relationships between numeric attributes.

### Cleaning:
- Dates were parsed into datetime format, and cyclic features for months and days were created to capture the cyclical nature of dates.
- Missing values in categorical variables were filled with the mode, and those in numeric variables with the median of the column.

## Data Preprocessing

Steps included:
- Label encoding categorical variables.
- Scaling features using `StandardScaler`.
- Detecting and dropping outliers based on analysis.

## Model Building

An artificial neural network (ANN) was built with the following configuration:
- Input layer with 26 features.
- Several hidden layers with `relu` activation and dropout layers to prevent overfitting.
- Output layer with a sigmoid activation function for binary classification.

The model was compiled with Adam optimizer and binary crossentropy loss. After training with early stopping, the model achieved good performance on both training and validation sets.

## Conclusion

The model's performance was evaluated on the test set using a confusion matrix and classification report. It showed high accuracy in predicting rain the next day, with good precision and recall for both classes.

## End

This project demonstrated the effectiveness of neural networks in predicting binary outcomes based on historical weather data. Further improvements could include hyperparameter tuning, using more complex models, or incorporating additional data sources.
