# Used-Vehicle-Price-Prediction

This repository contains the analysis and predictive modeling project for determining the prices of used vehicles. The goal is to assist a used car dealership in understanding key factors that influence vehicle prices and leveraging these insights for pricing strategies and inventory management.

## Project Structure
•	Jupyter Notebook: Used_Vehicle_Prices.ipynb contains all the code, analysis, and results.
•	Data: Preprocessed and cleaned data is used for modeling, including detailed imputation, outlier handling, and feature transformations.
•	ReadMe: Summary of the project and findings, with directions for reproducing the analysis.

## Summary of Findings

### Business Context
•	Objective: Develop a linear regression model to predict used vehicle prices.
•	Use Case: Provide actionable insights to a dealership for competitive pricing and inventory decisions.

### Data Summary
•	Dataset: 426,880 rows, 17 columns.
•	Response Variable: Vehicle price (transformed to price_sqrt for normality).
•	Key Predictors:
	•	Numerical: Year, odometer.
	•	Categorical: Fuel type, vehicle type, transmission, state region, etc.

### Key Insights
1.	Year and Odometer:
	•	Newer vehicles with lower mileage are priced higher.
2.	Fuel Type:
	•	Diesel and electric vehicles generally command premium prices.
3.	Vehicle Type:
	•	Pickups and SUVs are more expensive compared to sedans and hatchbacks.
4.	Regional Influence:
	•	Vehicles from the southern U.S. are priced higher due to better overall condition (less exposure to winter road salt).

## Model Highlights
•	The best-performing model is a multiple linear regression using all predictors after cleaning and feature engineering.
•	Performance Metrics:
	•	R²: [Insert value]
	•	RMSE: [Insert value]

## Repository Contents
•	Notebook:
	•	Structured with clear sections for business understanding, data understanding, preparation, modeling, evaluation, and deployment.
•	Data:
	•	Preprocessing steps are detailed in the notebook.
•	No Unnecessary Files:
	•	All files and directories are logically named and relevant to the project.

## Further Improvements
•	Enhance the model by exploring non-linear relationships using advanced machine learning algorithms.
•	Incorporate external data such as market trends or fuel prices for richer insights.
•	Use sequential feature selection on the final model to try to reduce overfitting

## Contact

For any questions or collaborations, please contact [Denali Carpener/denalicarpenter@gmail.com].