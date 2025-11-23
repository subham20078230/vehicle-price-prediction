Vehicle Price Prediction Project
📌 Overview

This project focuses on building a machine learning system that predicts vehicle prices based on various specifications such as make, model, year, engine details, mileage, fuel type, and more.
By exploring and analyzing the dataset, we aim to understand which features influence vehicle prices and develop a predictive model capable of estimating prices accurately.

📂 Dataset Description

The dataset contains detailed information about vehicles listed for sale. Below is an explanation of each feature:

Vehicle Features

name – Full name of the vehicle, including make, model, and trim.

description – Short vehicle description with key selling points.

make – Manufacturer of the vehicle (e.g., Toyota, Ford, BMW).

model – Model name of the vehicle.

year – Year the vehicle was manufactured.

price – Market price of the vehicle in USD (target variable).

engine – Engine details such as size, type, and configuration.

cylinders – Number of engine cylinders.

fuel – Fuel type (e.g., Gasoline, Diesel, Electric).

mileage – Total distance traveled, usually in miles.

transmission – Transmission type (Automatic, Manual, CVT).

trim – Trim level or package (e.g., SE, Limited, Premium).

body – Body style of the vehicle (SUV, Sedan, etc.).

doors – Number of doors.

exterior_color – Exterior paint color.

interior_color – Interior color/material.

drivetrain – Drivetrain configuration (AWD, FWD, RWD).

🎯 Project Objective

The primary objective is to:

✔ Understand and analyze the dataset
✔ Engineer useful features
✔ Preprocess and prepare data for modeling
✔ Build a machine learning model to predict car prices
✔ Evaluate model performance
✔ Save the trained model for future predictions

🧪 Exploratory Data Analysis (EDA)

Key steps included:

Checking missing values

Understanding numerical distributions (price, year, mileage, cylinders)

Analyzing categorical distributions (make, fuel, transmission, body)

Studying relationships between features and vehicle price

Creating visualizations such as:

Price distribution

Mileage distribution

Price by make

Price by body type

Fuel and transmission categories

Correlation heatmap

This helped identify trends and prepare the data for modeling.

🛠️ Feature Engineering

To improve the model, additional derived features were created:

Age → Calculated from manufacturing year

Cleaned mileage → Removing commas and converting to numeric

Engine liters → Extracted numeric engine size from text (e.g., “2.5L” → 2.5)

These new features provided more meaningful inputs for the model.

⚙️ Data Preprocessing

A preprocessing pipeline was built using sklearn:

Numeric features

Median imputation

Standardization

Categorical features

Most frequent imputation

One-hot encoding

This ensured the dataset was clean and fully ready for ML algorithms.

🤖 Model Development

The model used in this project:

RandomForestRegressor

Chosen because it:

Works well with mixed numeric/categorical features

Handles non-linear patterns

Is robust to outliers and noise

The model was trained on 80% of the data and tested on 20%.

📈 Model Evaluation

The model was evaluated using:

R² Score – Measures how well the model explains price variance

MAE (Mean Absolute Error) – Average error in predicted vs actual price

RMSE (Root Mean Squared Error) – Measures error magnitude

These metrics indicate how well the model performs at predicting vehicle prices.

💾 Saving the Model

The final trained model was saved using:

joblib.dump(model, "vehicle_price_model.joblib")


This allows future predictions without retraining.

🔮 Predicting New Vehicle Prices

To predict the price of a new car:

Prepare a dictionary of vehicle attributes

Apply the same feature engineering

Use the saved model to generate price prediction

Example:

price = model.predict(new_car)

📊 Technologies Used

Python

pandas

NumPy

scikit-learn

Matplotlib / Seaborn

Jupyter Notebook

📌 Conclusion

This project demonstrates how to:

✔ Analyze a structured vehicle dataset
✔ Engineer meaningful features
✔ Build and evaluate a machine learning pipeline
✔ Predict vehicle prices accurately

You can extend it by:

Using XGBoost or LightGBM

Hyperparameter tuning

Adding text analysis from description

Deploying the model as an API or web app
