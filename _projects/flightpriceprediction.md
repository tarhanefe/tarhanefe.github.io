---
title: 'Flight Price Prediction using ML Techniques Written From Scratch'
date: 2022-04-01
permalink: /projects/flightpriceprediction
image: "https://github.com/tarhanefe/tarhanefe.github.io/assets/73281981/6b0556ed-1990-432f-9d01-38e8f3dd94f0"
teaser: "https://github.com/tarhanefe/tarhanefe.github.io/assets/73281981/6b0556ed-1990-432f-9d01-38e8f3dd94f0"
---
This project explores the relationship between airline ticket prices and various factors such as airline, destination, flight times, booking period, and flight class. We developed custom-built machine learning models using fundamental Python libraries (numpy, pandas) to predict ticket prices based on these features.

## Dataset Description

The dataset contains the price of plane tickets from six Indian airline companies for flights between six major cities in India. The features include:

1. **Airline**: Categorical values for airline names.
2. **Flight**: Categorical flight codes (removed during preprocessing).
3. **Source City**: Categorical values for the departure cities.
4. **Departure Time**: Categorical time labels for departure time.
5. **Stops**: Categorical values for the number of stops.
6. **Arrival Time**: Categorical time labels for arrival time.
7. **Destination City**: Categorical values for the destination cities.
8. **Class**: Categorical values indicating if the flight is "economy" or "business" class.
9. **Duration**: Continuous feature representing flight duration.
10. **Days Left**: Continuous feature representing how many days before the flight the ticket was bought.
11. **Price**: Continuous variable and target for prediction.

## Data Analysis

- **Correlation Matrix**: Analyzed relationships between features using a heatmap.
- **Box Plots**: Examined relationships between flight prices and airlines, number of days before buying the ticket, and ticket classes.
- **Violin Plots**: Compared ticket prices for different flight classes.
- **Line Plots**: Visualized how ticket prices change as the departure date approaches.

## Applied Methods

### Linear Regression

Implemented linear regression using numpy to fit the model. The following methods were used:

- **Ordinary Least Squares (OLS)**: Basic linear regression method.
- **Ridge Regression**: Added L2 regularization to reduce overfitting.
- **Lasso Regression**: Added L1 regularization to produce a sparse model.

Performance metrics:
- **RMSE**: Root Mean Squared Error
- **R²**: Coefficient of Determination

### K-Nearest Neighbors (KNN)

Used KNN to assign predictions to new data points based on the average response values of the k-nearest training data points.

### Decision Trees

Constructed decision trees to segment the predictor space into finite regions, each associated with a prediction value. Applied bagging to improve performance by averaging over multiple trees.

### Neural Networks

Built and trained neural networks to capture nonlinear relationships in the data. Implemented stochastic gradient descent for training.

## Results

- **Linear Regression**:
  - OLS: RMSE = 21973.28, R² = 0.061
  - Ridge Regression: RMSE = 21961.37, R² = 0.0609
  - Lasso Regression: RMSE = 21965.48, R² = 0.0605
- **KNN**: RMSE = 3780.50
- **Decision Trees**:
  - Simple Decision Tree: RMSE = 4494.55
  - Bagging Decision Tree: RMSE = 4341.66
  - Random Forest: RMSE = 22661.89
- **Neural Networks**:
  - Single Perceptron: RMSE = 13893.22
  - Neural Network without Hidden Layer: RMSE = 4422.97
  - Neural Network with 1 Hidden Layer: RMSE = 4636.13

## Challenges Faced

- **Underfitting**: Due to a large number of data points and a relatively small number of predictors.
- **Training Time**: Extensive training times for more complex models.

## Conclusion

Among the methods tested, the KNN and decision tree models performed the best. Linear regression methods were limited by their inability to capture nonlinear relationships in the data, while neural networks showed promise but required extensive training time to optimize.

## Authors

- Kemal Enes Akyüz - 22003521
- Efe Tarhan - 22002840

## References

1. Bathwal, Shubham. "Flight Price Prediction." Kaggle. Accessed November 17, 2023. [Online]. Available: [Kaggle](https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction).
2. E. Dougherty, "Deciphering the Digits in Your Flight Number," Blue Sky PIT News Site, 09 Mar, 2020. Accessed: 18 Nov 2023. [Online]. Available: [Blue Sky PIT](https://blueskypit.com/2020/03/09/deciphering-the-digits-in-your-flight-number/)
3. Newcastle University, “Coefficient of Determination (R squared),” 2023. Accessed: 19 Nov 2023. [Online]. Available: [Newcastle University](https://www.ncl.ac.uk/webtemplate/ask-assets/external/maths-resources/statistics/regression-and-correlation/coefficient-of-determination-r-squared.html)
4. D. Witten and G. James, An introduction to statistical learning with applications in R. Springer publication, 2013.


[Link to the Github Repository](https://github.com/tarhanefe/Flight-Price-Prediction)

