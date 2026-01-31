📊 Retail Sales Forecasting System
An end-to-end forecasting engine designed to help retail businesses transition from reactive to proactive decision-making. This tool predicts monthly sales 6 months into the future, providing data-backed confidence for inventory, staffing, and budgeting.

🛠 Business Problem
Retailers often struggle with the "Bullwhip Effect," where inaccurate demand forecasting leads to:

Overstocking: Tied-up capital and high storage costs.

Understocking: Missed revenue opportunities and poor customer retention.

This project solves this by delivering a probabilistic forecast—giving businesses not just one number, but a range of possibilities (Conservative vs. Aggressive).

🚀 Key Features
Universal Data Ingestion: Dynamic column mapping allows users to upload any CSV regardless of column naming conventions.

Automated Seasonality: Built-in detection for US holidays and recurring annual retail cycles (e.g., the "Christmas Spike").

Accuracy Tracking: Real-time calculation of MAPE (Mean Absolute Percentage Error) and Model Accuracy.

Interactive Strategy Guide: Categorical filtering to isolate specific departments (e.g., Electronics vs. Furniture).

🧠 The Approach
Exploratory Data Analysis (EDA): Performed seasonal decomposition to isolate the trend from the "noise" of monthly fluctuations.

Modeling: Evaluated multiple models (XGBoost, ARIMA, Prophet). Prophet was selected for its superior handling of holiday effects and its ability to work well with smaller datasets (~4 years of data).

Validation: Used a temporal train/test split to ensure the model could generalize to future months.

📈 Technical Insights
MAPE: 10.2% (The model is ~90% accurate on historical trends).

Seasonality: Identified a consistent ~60% sales surge during Nov-Dec.

Growth: Captured a steady 15% YoY growth trend, allowing for scaling predictions.

💻 Tech Stack
Language: Python

Forecasting: Facebook Prophet

Data Processing: Pandas, NumPy

Frontend: Streamlit

Visualization: Matplotlib, Plotly

🏁 Key Takeaways
Simplicity Wins: For retail, domain-specific models (Prophet) often outperform complex black-box models (XGBoost) because they respect the human nature of shopping cycles.

Uncertainty is an Asset: Showing the "Lower Bound" and "Upper Bound" is more useful for a CFO than a single point prediction.
