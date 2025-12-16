# Ideal Booking Day Estimator for Flights

Airline ticket prices often seem unpredictable. Existing platforms such as Google Flights and
Skyscanner do not give recommendation on how the prices **will
change concerning different booking dates** for the same flight.

Given a user input of a specific date of flight, our goal is to predict the optimal day to purchase the ticket (that is, the day on
which the fare is lowest). Our work is distinct from most of the prior airline fare prediction research, because it optimizes **_when to book a given flight_**, rather than **_which  flight to choose_**.


## Summary

- **Data Source:** Expedia Flight Prices dataset (Kaggle), containing North American flights between April 2022 and October 2022.
- **Model:** XGBoost (Gradient Boosted Trees) and Ridge Regression.
- **Preprocessing:** Interpolation of missing values, feature engineering (calendar-based features), and normalization.
- **Evaluation:** Mean Absolute Error (MAE).
- **Results:** XGBoost outperforms Ridge Regression in predicting fare evolution. The best model achieved a test **MAE of 52 dollars**.

## Paper
**[Link](https://drive.google.com/file/d/1etEO4iy_NwO04r_AjLC9vBM8Gl8hIVIn/view?usp=sharing)** to **derived paper**
