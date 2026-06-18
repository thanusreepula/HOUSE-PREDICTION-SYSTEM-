# HOUSE-PREDICTION-SYSTEM-

A binary classification project that predicts whether a house will sell above or below the median market price, based on its physical features. Built in Google Colab using a Random Forest Classifier.

# Problem/Goal

Rather than predicting an exact sale price, this project frames the task as a classification problem: given a house's features, will it sell at or below the median price ("will sell") or above it ("won't sell")? This makes the problem easier to evaluate with standard classification metrics and is a common simplification when exact price regression isn't the goal.

# Dataset

A CSV of 4,600 house sale records with 10 columns, loaded from Google Drive: date, price, bedrooms, bathrooms, sqft_living, sqft_lot, floors, waterfront, view, and condition. There were no missing values in any column.

Two engineered fields were added before modeling:
year_sold, extracted from the date column (the original date column was then dropped).
will_sell, the binary target: 1 if price is at or below the dataset median (~$460,943), 0 otherwise. This produces a perfectly balanced target (2,300 vs. 2,300).
Final feature set used by the model: bedrooms, bathrooms, sqft_living, sqft_lot, floors, waterfront, view, condition, year_sold.

# Tech Stack
Python
pandas
scikit-learn — RandomForestClassifier (100 estimators), train_test_split, accuracy_score, classification_report
Google Colab + Google Drive (data storage and loading)


# How to Run It
Open HOUSE_PRICE_PREDICTION.ipynb in Google Colab.
Mount your Google Drive when prompted.
Update the CSV file path in the data-loading cell to point to your own copy of the dataset.
Run all cells in order: data loading → cleaning → feature engineering → train/test split (80/20, random_state=42) → model training → evaluation → sample prediction → feature importance.
