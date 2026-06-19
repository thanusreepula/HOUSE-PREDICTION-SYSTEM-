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
Python(pandas ,scikit-learn )
Google Colab 

# How to Run It
1. Download HOUSE_PRICE_PREDICTION.ipynb from this repo, and download the dataset CSV
2. Go to Google Colab and upload the notebook (File → Upload notebook).
3. Upload the dataset CSV to your own Google Drive.
4. Run the first cell — it will prompt you to authorize Google Drive access. Allow it.
5. Find the cell with pd.read_csv(...) and update the file path to match where you placed the CSV in your Drive
6. Run all cells in order
7. If you hit a FileNotFoundError, double-check the path in step 5 matches exactly where the file sits in your Drive.
