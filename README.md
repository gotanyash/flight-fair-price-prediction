# Flight Fare Price Prediction
## Project Overview
Flight ticket prices are notoriously unpredictable. Prices can fluctuate drastically based on factors like timing, demand, and route. This project demonstrates how machine learning can be leveraged to predict flight fares accurately, using a dataset containing flight details between March and June 2019. The end goal is to create a predictive model that captures the intricate dynamics of flight pricing.

## Problem Statement
Flight ticket prices often change unexpectedly. Travelers frequently complain about their unpredictability. With the right dataset, however, we can model and predict these prices effectively. In this project, we aim to analyze and predict flight fares using a dataset of 10,682 records for training and 2,671 records for testing.

## Dataset Information
**Features in the Dataset:**
- **Airline**: Name of the airline.
- **Date_of_Journey**: Date of travel.
- **Source**: Starting location of the flight.
- **Destination**: Ending location of the flight.
- **Route**: The flight's route to the destination.
- **Dep_Time**: Departure time from the source.
- **Arrival_Time**: Time of arrival at the destination.
- **Duration**: Total travel time of the flight.
- **Total_Stops**: Number of stops between the source and destination.
- **Additional_Info**: Miscellaneous information about the flight.
- **Price**: Ticket price in Indian Rupees (Target variable).

## Challenges Faced with Data
1. **Missing Data**:
   - Missing values in columns like "Total_Stops" and "Route" required careful handling via imputation or removal.
2. **Data Format Inconsistencies**:
   - Date and time fields were stored as strings, requiring conversion to datetime format for effective analysis.
3. **Categorical Data**:
   - Columns like "Airline" and "Source" needed one-hot encoding to make them suitable for machine learning models.
4. **Outliers**:
   - Extreme ticket prices were identified and addressed to reduce their impact on model accuracy.

## Techniques and Justification
### Data Preprocessing:
- **Datetime Conversion**: Transformed "Date_of_Journey," "Dep_Time," and "Arrival_Time" into datetime objects.
- **Handling Missing Values**: Missing data in "Total_Stops" was imputed using the mode.
- **Encoding Categorical Variables**: Used one-hot encoding to convert categorical features into numerical format.

### Feature Engineering:
- **Extracting Journey Day and Month**: Added new features from "Date_of_Journey" to capture temporal patterns in flight fares.
- **Flight Duration Calculation**: Calculated total duration from "Dep_Time" and "Arrival_Time."

### Model Selection:
- **Model Used**: Random Forest Regressor.
  - Chosen for its ability to handle nonlinear relationships and categorical variables effectively.
  - Provides feature importance metrics, aiding in identifying key predictors.
- **Hyperparameter Tuning**: Performed to optimize parameters and improve model performance.

## Results and Insights
- The **Random Forest model** achieved acceptable accuracy levels, demonstrating its ability to capture complex, nonlinear patterns in flight pricing.
- Challenges such as missing data, outliers, and categorical variables were successfully addressed, ensuring data quality and improving model performance.
