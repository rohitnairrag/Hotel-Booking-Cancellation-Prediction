This Jupyter Notebook predicts hotel booking cancellations using machine learning. It analyzes the INNHotelsGroup_pastdata.csv dataset, containing booking details like lead time, market segment, special requests, room price, number of adults, weekend/weekday nights, arrival date, parking needs, booking status, and rebooking data.
The notebook preprocesses data by handling missing rebooked values, converting arrival_date to datetime, and creating arrival_year and arrival_month features. The required_car_parking_space column is transformed into a categorical variable. Exploratory data analysis (EDA) reveals patterns, such as correlations between lead time, special requests, and cancellations.
Several models are implemented to predict cancellations (Canceled vs. Not Canceled):

Logistic Regression (statsmodels and scikit-learn)
Decision Tree (with and without pre-pruning)
Random Forest (default and tuned with GridSearchCV)

Models are evaluated on accuracy, precision, recall, and F1 score, with the tuned Random Forest achieving the best F1 score (0.6314). The workflow includes one-hot encoding for categorical variables, train-test splitting, and hyperparameter tuning.
Ideal for hospitality analytics and machine learning enthusiasts, this project showcases data preprocessing, feature engineering, model building, and evaluation. It uses pandas, numpy, matplotlib, seaborn, scikit-learn, and statsmodels.
Usage: Clone the repo, ensure the dataset is available, and run the notebook in a Python environment with required libraries.
Keywords: Hotel booking, cancellation prediction, machine learning, logistic regression, decision tree, random forest, data preprocessing, feature engineering, GridSearchCV, hospitality analytics.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

| `booking_id`                 | Unique identifier for each booking. Usually alphanumeric or numeric.                                                 |
| `lead_time`                  | Number of days between booking date and arrival date. High values may indicate early planning.                       |
| `market_segment_type`        | Type of market segment (e.g., Online, Corporate, Offline, Aviation, etc.). Helps identify the source of the booking. |
| `no_of_special_requests`     | Number of special requests (e.g., late checkout, high floor, etc.) made by the customer.                             |
| `avg_price_per_room`         | Average daily price per room for that booking. Reflects hotel pricing strategy.                                      |
| `no_of_adults`               | Number of adults in the booking.                                                                                     |
| `no_of_weekend_nights`       | Number of weekend nights (typically Friday and Saturday) included in the stay.                                       |
| `arrival_date`               | Date when the guest is scheduled to arrive. May be in `dd/mm/yyyy` or `yyyy-mm-dd` format.                           |
| `required_car_parking_space` | Whether a car parking space was requested (usually 0 = No, 1 = Yes).                                                 |
| `no_of_week_nights`          | Number of weekdays (Sunday to Thursday) the guest is staying.                                                        |
| `booking_status`             | Status of the booking — for example, `Canceled` or `Not_Canceled`.                                                   |
| `rebooked`                   | Indicates whether the guest rebooked after a cancellation (1 = Yes, 0 = No). Useful for customer loyalty analysis.   |
