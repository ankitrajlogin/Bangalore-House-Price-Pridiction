# Bangalore-House-Price-Pridiction
This project utilizes machine learning techniques, specifically linear regression, to predict home prices in Bangalore, India. The model is trained on a dataset containing various features of homes in Bangalore such as location, total square feet, number of bedrooms, etc.

## Steps Followed

1. **Data Load**: The Bangalore house prices dataset is loaded from a CSV file.
2. **Drop Unnecessary Features**: Features that are not required to build the model are dropped.
3. **Data Cleaning**: Any missing values (NA) are handled.
4. **Feature Engineering**:
   - Added a new feature for BHK (Bedrooms Hall Kitchen).
   - Examined and processed the 'total_sqft' feature by taking averages of range data.
   - Added a new feature called 'price per square feet' for further data preprocessing.
5. **Location Examination**: 
   - Locations, being categorical variables, are examined. Dimensionality reduction techniques are applied to reduce the number of locations.
6. **Outlier Removal Using Business Logic**:
   - Removed outliers based on the business logic that typically 1 square ft per bedroom is 300 sqft. 
   - Outliers with suspicious square footage for the number of bedrooms are removed.
7. **Outlier Removal Using Standard Deviation and Mean**:
   - Outliers are removed per location using mean and one standard deviation.
   - Properties with illogical price disparities within the same location are removed.
8. **Outlier Removal Using Bathrooms Feature**:
   - Properties with an unusually high number of bathrooms per bedroom are removed.
9. **Dropping Extra Features**: Unnecessary features are dropped.
10. **One Hot Encoding For Location**: Location data is encoded using one-hot encoding.
11. **Building Model using Linear Regression**: Linear regression model is built.
12. **K Fold Cross Validation**: Cross-validation is used to measure the accuracy of the linear regression model.
13. **Find Best Model Using GridSearchCV**: GridSearchCV is employed to find the best model.
14. **Export Model to a Pickle File**: The tested model is exported to a pickle file.

## Usage

1. Ensure all dependencies mentioned should be installed.
2. Run the Python script containing the model building and prediction code.
3. Provide input features (e.g., location, total square feet, number of bedrooms) for the prediction.
4. Get predicted home prices for the given input.

## Files Included

- `bangalore_house_prices.csv`: Dataset containing Bangalore house prices.
- `bangalore_home_prices_code.ipynb`: Python script containing the model building and prediction code.
- bangalore_home_prices_model.sav : Saved model that can directly use
- columns.json : Export location and column information to a file that will be useful in our prediction application


## Dependencies

- Python 3.x
- NumPy
- Pandas
- Scikit-learn
