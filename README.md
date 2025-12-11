Car Price Prediction Using Statistical Methods – Project Overview (Student Version)
=> Introduction

The aim of this project is to understand which factors affect the price of a car and how accurately we can predict car prices using statistical techniques.
I used the Car Price Assignment dataset, which contains various car features such as engine size, horsepower, curb weight, fuel type, car body, and brand.

The main idea was to check:

Which car features influence the price the most?

Can we build a statistical model that predicts car price?

Are all the variables significant or only a few important ones?

How does the full model compare with reduced models?

🛠️ Tools & Libraries Used

Python

Pandas

NumPy

Seaborn

Matplotlib

Statsmodels

SciPy

scikit-learn

Jupyter Notebook

📂 Dataset Description

The dataset contains 205 rows and various attributes of cars, such as:

Car brand (CarName)

Engine size

Horsepower

Body type

Fuel system

Number of cylinders

Curb weight

Price (target variable)

Some columns were messy (brand names misspelled), so I cleaned and encoded them before performing any analysis.

 1. Data Cleaning & Preparation

Extracted the car brand from the CarName column

Corrected spelling mistakes (e.g., vokswagen → volkswagen)

Converted all categorical columns using LabelEncoder

Removed columns with no correlation or irrelevant info (car_ID, compressionratio, symboling, peakrpm)

Verified dataset shape and confirmed all columns were numeric

 2. Correlation Analysis

I plotted a correlation heatmap to find out which features strongly relate to car price.

Key observations:

Engine size, horsepower, and curb weight had the strongest positive correlation with price

Body type and brand had weaker correlation

After cleaning, the heatmap was fully filled and visually clear

This step helped identify which variables to include in the regression model.

📉 3. Multiple Linear Regression

I built an OLS regression model using:

price ~ enginesize + horsepower + curbweight + carbody + CarName + cylindernumber

 Results:

Engine size and horsepower were the most significant predictors

Curb weight also had a meaningful effect

The model had a good R² value, showing strong predictive power

All predictors had p-values < 0.05, meaning they significantly influenced car price

This means the model is statistically valid.

📊 4. Hypothesis Testing

I performed:

t-tests on each coefficient (to check individual significance)

z-test on car price mean

ANOVA (F-test) comparing simple vs. expanded models

What I found:

The full model performed much better than models with fewer variables

Adding horsepower after engine size significantly improved prediction

All predictors provided statistically meaningful information

 5. Actual vs Predicted Plot

I plotted the predicted prices vs. actual prices.

Most points were close to the diagonal red line

This shows the model fits the data well and predictions are quite accurate

Project team:
Amolika:24XVIM0528
Paridhi:24XV1M0533
Mahathi:24XV1M0558
Yashaswini:24XV1M0559
Shivani:24XV1M6624
Chiruhas:24XV1M0511
