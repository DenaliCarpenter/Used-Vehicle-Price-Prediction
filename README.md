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

The modeling process focused on predicting the square root of vehicle prices (price_sqrt) using a multiple linear regression model. This section outlines key results and additional insights derived from the analysis.

1. Model Performance

	•	Training Metrics:
	•	R² (Training): The model explained a substantial proportion of variance in the training dataset, indicating a good fit.
	•	MSE (Training): Low mean squared error on the training set confirms the model captured relationships effectively.
	•	Validation Metrics:
	•	R² (Validation): High R² (0.57) on the validation dataset suggests the model generalizes well to unseen data.
	•	RMSE (Validation): The root mean squared error indicates an average prediction error of approximately 63.7, highlighting the model’s practical utility.
	•	Test Metrics:
	•	On the held-out test set, the model demonstrated stable performance, with minimal deviation from training and validation metrics.

2. Key Predictors

The model’s coefficients and feature importance rankings revealed significant relationships between variables and vehicle prices:
	1.	Year:
	•	Positive correlation with price_sqrt. Newer vehicles have higher prices due to better condition, modern features, and remaining warranty periods.
	2.	Odometer:
	•	Negative correlation with price_sqrt. Lower mileage increases vehicle desirability and resale value.
	3.	Fuel Type:
	•	Diesel and electric vehicles consistently showed higher prices. Diesel vehicles are valued for fuel efficiency and longevity, while electric vehicles reflect growing demand for eco-friendly transportation.
	4.	Vehicle Type:
	•	Pickup trucks, SUVs, and coupes were the highest-priced categories on average, driven by their utility, style, and market demand.
	5.	Regional Effects:
	•	Vehicles from southern regions of the U.S. fetched higher prices, possibly due to better overall condition (e.g., less exposure to road salt in winter).

3. Insights from Model Results

	1.	Multicollinearity and Feature Selection:
	•	Regularization techniques like Ridge and Lasso regression highlighted redundancy in certain variables (e.g., drive and type).
	•	While all predictors added some explanatory power, reducing multicollinearity improved interpretability and prediction accuracy.
	2.	Non-linear Effects:
	•	Square root transformation of price revealed nuanced relationships that were not evident in the raw data.
	•	Non-linear trends were observed in the odometer feature, where extremely high mileage slightly dampened the price drop (e.g., classic cars with high mileage but collector value).
	3.	Interaction Effects:
	•	Exploring interactions, such as year × type or fuel × odometer, could reveal additional patterns. For example:
	•	Older SUVs might still retain higher prices compared to older sedans due to their durability and market demand.
	•	Electric cars with lower mileage command premium prices compared to their gas counterparts.
	4.	Categorical Predictors:
	•	One-hot encoded variables like fuel and type proved essential, capturing meaningful group-level differences that contributed significantly to the model’s explanatory power.

4. Model Limitations and Opportunities

	1.	Limitations:
	•	Linear Assumptions: Linear regression assumes additive effects, which may oversimplify relationships (e.g., odometer likely has diminishing returns).
	•	Feature Imputation: Imputed values for missing data may introduce bias or noise, particularly in features with high missingness (e.g., condition, cylinders).
	2.	Opportunities:
	•	Incorporating interaction terms and polynomial features could enhance the model’s ability to capture complex relationships.
	•	Ensemble methods (e.g., Random Forests or Gradient Boosting) could provide additional predictive power, albeit at the cost of interpretability.

5. Business Implications

	1.	Pricing Strategy:
	•	Use the model to identify undervalued vehicles and adjust pricing dynamically based on real-time inventory data.
	•	Prioritize acquiring vehicles with high resale value predictors (e.g., low mileage, diesel/electric fuel types, pickups/SUVs).
	2.	Regional Inventory Management:
	•	Allocate resources to source vehicles from regions with high demand but low supply, as identified through regional price trends.
	3.	Customer Segmentation:
	•	Target customer segments based on preferences for specific features (e.g., fuel-efficient vehicles, modern tech in newer models).

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