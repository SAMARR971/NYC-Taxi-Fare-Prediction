# NYC Taxi Fare Prediction

## Project Overview

This project focuses on predicting taxi fare amounts in New York City using real-world NYC Yellow Taxi trip data.

The project follows an end-to-end machine learning workflow, including data cleaning, exploratory data analysis, feature engineering, time-aware train-test splitting, model training, hyperparameter tuning, and model evaluation.

## Objective

The main objective is to develop machine learning models that can predict the `fare_amount` of a taxi trip based on information such as:

* Pickup and drop-off locations
* Trip distance
* Passenger count
* Date and time
* Trip duration-related information
* Other engineered features

## Dataset

The project uses publicly available NYC Yellow Taxi Trip Data.

Target variable:

```text
fare_amount
```

The dataset contains information about taxi trips in New York City, including pickup and drop-off locations, passenger count, datetime information, and fare amounts.

## Project Workflow

### 1. Data Loading and Exploration

* Loaded the NYC taxi dataset
* Examined dataset shape
* Checked data types
* Inspected sample records
* Investigated missing values and basic statistics

### 2. Data Cleaning

The dataset was cleaned by:

* Removing missing values
* Removing invalid fare values
* Filtering unrealistic passenger counts
* Removing invalid geographic coordinates
* Filtering unrealistic trip distances
* Removing extreme or incorrect observations

### 3. Feature Engineering

Several new features were created to improve model performance.

These include:

* Haversine trip distance
* Pickup hour
* Day of week
* Day
* Month
* Year
* Other time-based features

The Haversine formula was used to estimate the geographical distance between pickup and drop-off locations.

### 4. Exploratory Data Analysis

EDA was performed to investigate relationships between taxi fares and different features.

Visualizations were created to analyze:

* Fare distribution
* Trip distance vs. fare
* Fare variation by hour/time
* Other important relationships in the dataset

### 5. Time-Aware Train-Test Split

Instead of randomly splitting the data, the dataset was divided based on time.

Earlier trips were used for training, while later trips were used for testing.

This approach better represents a real-world prediction scenario and helps prevent information from the future being used to train the model.

## Machine Learning Models

Two main regression models were trained:

### Linear Regression

Linear Regression was used as the baseline model.

### Random Forest Regressor

Random Forest Regressor was used as the main machine learning model because it can capture nonlinear relationships between taxi trip features and fare amounts.

## Model Evaluation

The models were evaluated using:

### RMSE

Root Mean Squared Error measures the average prediction error in dollar units, with larger errors receiving greater weight.

### RMSLE

Root Mean Squared Logarithmic Error evaluates prediction error on a logarithmic scale and reduces the influence of very large fare values.

## Hyperparameter Tuning

Hyperparameter optimization was performed using:

* GridSearchCV
* RandomizedSearchCV

These techniques were used to find better parameter combinations for the machine learning model.

## Feature Importance

Feature importance was analyzed to understand which variables contributed most to taxi fare predictions.

The analysis helps explain what the Random Forest model learned from the data.

## Results

The performance of the models was compared using RMSE and RMSLE.

| Model               |            RMSE |           RMSLE |
| ------------------- | --------------: | --------------: |
| Linear Regression   | Add your result | Add your result |
| Random Forest       | Add your result | Add your result |
| Tuned Random Forest | Add your result | Add your result |

The best-performing model was selected based on the evaluation metrics.

## Conclusion

This project demonstrates a complete machine learning workflow for a real-world regression problem.

The project covers data preprocessing, feature engineering, exploratory data analysis, time-aware validation, machine learning, hyperparameter tuning, and model interpretation.

The results demonstrate how trip distance, geographic information, and time-related features can be used to predict taxi fare amounts.

## Limitations and Future Improvements

Possible improvements include:

* Using larger amounts of historical taxi data
* Adding weather information
* Adding traffic-related information
* Including airport and landmark features
* Testing advanced models such as XGBoost, LightGBM, or CatBoost
* Deploying the final model as a web application or API

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Machine Learning
* Regression
* GridSearchCV
* RandomizedSearchCV

## Project Structure


NYC-Taxi-Fare-Prediction/
│
├── NYC_Taxi_Fare_Prediction.ipynb
├── README.md
