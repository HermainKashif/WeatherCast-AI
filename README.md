# WeatherCast-AI
Weathercast AI is a machine learning-based weather prediction system that classifies daily weather conditions (rain, sun, fog, drizzle, snow) based on meteorological input parameters. The system uses two classification algorithms — K-Nearest Neighbors (KNN) and Random Forest — and compares their performance to provide the most accurate prediction. 

The project is built using Python with a user-friendly interactive web interface powered by Gradio, allowing users to adjust weather parameters via sliders and instantly receive predictions from both models. 
# Objectives: 
 Train KNN and Random Forest classifiers on real Seattle weather data

 Compare the accuracy of both models

 Build an interactive Gradio web interface for real-time weather prediction 

 Allow users to input weather parameters and receive instant predictions 
# Data Preprocessing: 
Before training the models, the dataset was cleaned and prepared. The date column was dropped since it is not a useful feature for prediction. The weather column distribution was analyzed to understand class balance. The date column is removed using df.drop(). The value_counts() function shows the distribution of weather classes: Rain (641), Sun (640), Fog (101), Drizzle (53), Snow (26). This confirms that the dataset is slightly imbalanced with Snow being the rarest class. 
# Train-Test Split: 
The dataset was split into 80% training and 20% testing using train_test_split() with a random_state of 42 for reproducibility
Feature Scaling: Since KNN is distance-based, feature scaling is critical. StandardScaler was applied to normalize the training data and then used to transform the test data with the same scale parameters. Note: Random Forest does not require scaling. 

# KNN achieved an accuracy of 74.1% on the test set. 
# Random Forest achieved an accuracy of 81.6% on the test set, outperforming KNN by 7.5%.
