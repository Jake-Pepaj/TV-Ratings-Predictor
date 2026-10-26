#Predictive Analysis of TV Show Ratings
This repository contains a machine learning pipeline designed to predict pre-release television show and movie ratings using a large-scale anime dataset. The project focuses on rigorous data preprocessing, feature engineering, and establishing a baseline predictive model for media performance.   

Data Preprocessing & Feature Engineering
- Data Cleaning: Filtered out unrated entries and removed irrelevant formats such as 'Music' and 'Radio'. Refined categorical noise by restricting the dataset to major production studios with over 40 entries and licensors with over 20 entries.
- Feature Engineering: Utilized regular expressions to parse show titles and engineered a new Series_Size feature to quantify franchise power and sequel groupings.
- Encoding: Applied one-hot encoding to categorical variables including Type, Source, Rating, Licensors, and Studios, while specifically expanding multi-label, comma-separated Genres into distinct binary columns.
- Normalization: Split the data into an 80/20 training and testing set, subsequently applying Z-score normalization (StandardScaler) to the Series_Size variable strictly post-split to prevent data leakage.

Baseline Model & Results
An initial LinearRegression model was trained on the preprocessed dataset to establish baseline predictive metrics.   
- Mean Absolute Error (MAE): 0.470
- Root Mean Squared Error (RMSE): 0.603
- Mean Squared Error (MSE): 0.364
- R-squared (R2): 0.342   
