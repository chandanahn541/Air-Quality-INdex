🌍 Air Quality Index (AQI) Prediction using Machine Learning

A machine learning mini-project that predicts the overall Air Quality Index (AQI) from individual pollutant AQI values using a Random Forest Regressor.

📌 Overview

Air quality is measured through the concentration of several pollutants. This project uses the AQI sub-index values of four major pollutants to predict the overall AQI value of a location.

Input features

Feature	Description
co aqi value	Carbon Monoxide AQI sub-index
ozone aqi value	Ozone AQI sub-index
no2 aqi value	Nitrogen Dioxide AQI sub-index
pm2.5 aqi value	Fine particulate matter (PM2.5) AQI sub-index

Target: aqi value (overall AQI)

📂 Dataset
File: air_quality_data.csv
Rows: 16,695
Columns: 7 (AQI Value, CO AQI Value, Ozone AQI Value, NO2 AQI Value, PM2.5 AQI Value, lat, lng)
Missing values: none
Latitude/longitude are present in the data but not used as model features.
⚙️ Workflow
Import libraries and load the dataset
Inspect shape, data types, and missing values
Preprocess: drop nulls, standardize column names (lowercase, stripped)
Exploratory Data Analysis: pair plot and correlation heatmap
Feature selection: 4 pollutant AQI values as X, overall AQI as y
Train-test split (80% / 20%, random_state=42)
Train a RandomForestRegressor (100 trees)
Evaluate with MAE, MSE, and R²
Plot actual vs predicted AQI
📊 Results
Metric	Score
Mean Absolute Error (MAE)	0.0894
Mean Squared Error (MSE)	2.5934
R² Score	0.9984

Note: The overall AQI is defined by the standard as the maximum of the individual pollutant sub-indices, so the pollutant values almost fully determine it. This is why the model reaches a very high R². To make this more challenging and realistic, future work could forecast AQI from weather data, location, and past readings.

🛠️ Tech Stack
Python 3
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Jupyter Notebook
🚀 Getting Started
1. Clone the repository
bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
2. Install dependencies
bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
3. Add the dataset

Place air_quality_data.csv in the same folder as the notebook.

4. Run the notebook
bash
jupyter notebook ML_mini-project_air-quality_index_.ipynb
🔮 Future Improvements
Compare with other models (Linear Regression, Gradient Boosting, XGBoost)
Hyperparameter tuning with GridSearchCV / RandomizedSearchCV
Add cross-validation for more robust evaluation
Plot feature importance
Include location and time features for true AQI forecasting
Save the trained model and deploy it as a Streamlit/Flask web app
📁 Repository Structure
├── ML_mini-project_air-quality_index_.ipynb
├── air_quality_data.csv
└── README.md
🤝 Contributing

Suggestions and improvements are welcome. Feel free to fork the repo and open a pull request.

📄 License

This project is open source and available under the MIT License.

👤 Author

Your Name GitHub: @chandanahn541
