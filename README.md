Traffic Prediction and Adaptive Navigation System

Overview

This project develops a machine learning-based system to predict traffic volumes in urban areas, specifically New York City, using historical and real-time data. The system employs XGBoost and Random Forest models to forecast traffic and integrates predictions into a Flask API for real-time user interaction. The goal is to optimize traffic flow, suggest alternative routes, and support urban planning by reducing congestion-related issues like delays and pollution.

Repository Contents





Final_Report__Traffic_Prediction_and_Adaptive_Navigation_System.docx: The final project report detailing the system design, methodology, results, and future work.



Dataset: Traffic volume data (2022–2024) from the New York City Department of Transportation (NYC DOT), including features like year, month, day, hour, street, direction, traffic volume, and weather conditions.



Code: Python scripts for data preprocessing, model training (XGBoost, Random Forest, Linear Regression), evaluation, and Flask API implementation (not included in the document but referenced as using scikit-learn, XGBoost, Flask, and pandas libraries).



Visualizations: Plots (e.g., feature importance, traffic volume distribution, correlation matrix) referenced in the report.

Prerequisites

To replicate or extend the analysis, ensure the following are installed:





Python 3.x



Libraries: pandas, scikit-learn, xgboost, flask, matplotlib



Dataset: Obtain traffic volume data from NYC DOT or equivalent source

Methodology





Data Preprocessing:





Cleaned dataset by handling missing values, removing invalid records, and addressing outliers.



Engineered features by encoding categorical variables (e.g., street, direction) and scaling numerical features.



Split data into 80% training and 20% testing sets.



Model Training:





Trained three models: Linear Regression, Random Forest, and XGBoost.



Optimized XGBoost through hyperparameter tuning for best performance.



Evaluation:





Used RMSE (Root Mean Squared Error) and R² (R-squared) to assess model performance.



Visualized results with feature importance plots, traffic volume distributions, and correlation heatmaps.



API Integration:





Built a Flask API to serve real-time traffic predictions based on user inputs (e.g., time, location, weather).



Developed a simple HTML/JavaScript frontend for user interaction.

Key Findings





Model Performance:





XGBoost: Best performer with RMSE = 95.34, R² = 0.907 after tuning.



Random Forest: RMSE = 100.53, R² = 0.825.



Linear Regression: Underperformed with RMSE = 172.95, R² = 0.0357 due to nonlinear data.



Key Features: Hour, street, and weather conditions were the most influential predictors of traffic volume.



API: Successfully delivered real-time predictions, suitable for integration into navigation systems or traffic management tools.



Insights: Traffic peaks during morning and evening rush hours, with strong correlations between traffic volume, time, and street direction.

Usage





Clone the repository (if available) or download the report and dataset.



Install required Python libraries: pip install pandas scikit-learn xgboost flask matplotlib.



Preprocess the dataset as described in the report (cleaning, encoding, scaling).



Run model training scripts to replicate XGBoost, Random Forest, or Linear Regression results.



Deploy the Flask API:





Run the Flask server: python app.py.



Access the HTML interface or send POST requests to the API endpoint with parameters (e.g., time, street, weather).



Visualize results using provided plot descriptions (e.g., traffic volume histograms, feature importance).

Limitations





Limited to NYC DOT data (2022–2024), which may not generalize to other cities.



Excludes real-time factors like road incidents or construction events.



Basic HTML interface lacks advanced visualization (e.g., map-based predictions).

Future Work





Integrate additional real-time data (e.g., accidents, construction, weather updates).



Enhance scalability by deploying on cloud platforms (e.g., AWS, Google Cloud).



Develop a more interactive frontend with map-based visualization for route suggestions.

References





NYC DOT Traffic Volume Counts: https://www.nyc.gov/dot



Chen, T., & Guestrin, C. (2016). XGBoost: A Scalable Tree Boosting System. KDD '16.



Breiman, L. (2001). Random Forests. Machine Learning, 45(1).



Python libraries: scikit-learn, xgboost, flask.