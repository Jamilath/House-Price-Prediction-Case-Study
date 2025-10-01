Overview
This repository contains a comprehensive Data Science project analyzing real estate data from Makaan.com to predict house prices. Developed as part of a case study (completed on October 01, 2025), it showcases end-to-end workflows: data loading, cleaning, Exploratory Data Analysis (EDA), machine learning modeling, and interactive visualization using Power BI.

Objective: Load 332,096 real estate listings, deduplicate to 207,363 rows, predict prices with a Random Forest model (R2=0.995), and build a dashboard for market insights.
Tools: Python (pandas, sklearn, sqlalchemy, matplotlib, seaborn), MySQL Workbench, Jupyter Notebook, Power BI.
Dataset: Makaan_Properties_Details.csv and Makaan_property_location_details.csv (sourced from Makaan.com, 2020-2022 data).
Key Features: Handled relative dates ("2 months ago"), fixed 103,752 blanks in builder_id/Builder_name with "Unknown"/0, optimized GridSearchCV.

Setup Instructions

Prerequisites:

Python 3.8+
MySQL Server (with database "real_estate")
Power BI Desktop
Git (for cloning)
Libraries: pandas, sklearn, sqlalchemy, matplotlib, seaborn (install via pip install -r requirements.txt if added).


Database Setup:

Install MySQL, create "real_estate" database.
Load Makaan_Properties_Details.csv and Makaan_property_location_details.csv using the Python script (house_price_prediction.ipynb).
Update MySQL credentials in the script (e.g., root:Maleeha25*).


Clone Repository:#https://github.com/Jamilath/House-Price-Prediction-Case-Study

Run Jupyter Notebook:

Open house_price_prediction.ipynb in Jupyter Notebook.
Execute cells to replicate data loading, EDA, modeling, and predictions.


Power BI Dashboard:

Open house_price_dashboard.pbix in Power BI Desktop.
Refresh data connection to MySQL (update credentials if needed).
Explore interactive visuals.



Usage

EDA & Modeling: Use the Jupyter Notebook to regenerate plots (e.g., price_distribution.png) and train the Random Forest model.
Predictions: Check predicted_prices table in MySQL or temp_predictions.png for sample outputs.
Dashboard: Navigate Power BI pages (Executive Summary, Location Analysis, Builder Insights, Market Trends) to analyze KPIs, trends, and predictions (82.37% accuracy).

Project Files

house_price_prediction.ipynb: Main Python script for data loading, EDA, modeling.
house_price_prediction.html: Exported HTML version of the notebook.
house_price_dashboard.pbix: Power BI dashboard file.
LLD_House_Price_Prediction.docx: Low-Level Document detailing the project.
House_Price_Prediction.pptx: Presentation slides.
outputs.txt: Jupyter logs.
mysql_outputs.txt: MySQL query results.
joined_data.csv: Joined dataset post-EDA.
house_price_model.pkl: Trained Random Forest model.
PNGs: Visualizations (price_distribution.png, price_by_city.png, etc.).
temp_predictions.png: Screenshot of predicted prices.
Makaan_Properties_Details.csv, Makaan_property_location_details.csv: Source data.

Results

Data Cleaning: Deduplicated 161,995 rows, handled 103,752 blanks in builder_id/Builder_name.
Model Performance: R2=0.995, MSE=12,074,644,591,108.43, MAE=186,411.06; top features: Price_per_unit_area (0.69), Size (0.30).
Dashboard Insights: 101K properties, ₹14.32M avg price, Mumbai dominates (51K listings), 82.37% prediction accuracy.
Challenges Resolved: Relative date parsing, MySQL safe mode, slow GridSearchCV (~31 minutes).


