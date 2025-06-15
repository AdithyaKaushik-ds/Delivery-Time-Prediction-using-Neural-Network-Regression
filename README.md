# Delivery-Time-Prediction-using-Neural-Network-Regression

This project focuses on building a neural network regression model to accurately predict delivery times based on historical logistics data. Accurate time estimates are crucial for improving user experience and operational efficiency in last-mile delivery services.

📌 Problem Statement

To develop a machine learning pipeline—specifically using neural network regression—to predict delivery time in minutes based on various operational and order-related features.

🔍 Exploratory Data Analysis (EDA)

Conducted thorough EDA including univariate and bivariate visualizations (boxplots, scatterplots, histograms).

Extracted time features (hour, weekday) and engineered delivery duration from timestamps.

Identified peak order hours (2–3 AM) and highest order day (Saturday).

Handled missing values and eliminated outliers using IQR-based filtering.

🛠️ Feature Engineering & Preprocessing

Derived features such as time_taken_mins, order_hour, and weekday.

Encoded categorical variables and applied MinMax/Standard scaling for model readiness.

Outlier handling was performed using visual (boxplots) and statistical methods (IQR).

🤖 Models Developed

Random Forest Regressor

R² Score: 0.24

MAE: ~10.0 min

RMSE: ~12.6 min

Baseline Neural Network

3 Hidden Layers: 256 → 128 → 64 neurons

Optimizer: Adam, Loss: MSE

R² Score: ~0.23, MAE: ~9.95 min

Optimized Neural Network (via manual hyperparameter tuning)

Best Params: 128 neurons/layer, 0.001 LR, 64 batch size, 50 epochs

Regularization: L1_L2 + EarlyStopping

Final MAE: ~10.15 min, MAPE: ~24.19%

📈 Visuals & Interpretations

Visualizations included feature importance (Random Forest), training-validation loss curves, and prediction vs actual scatter plots.

Delivery time was most impacted by item quantity, order protocol, and peak order hours.

✅ Conclusion

The neural network achieved comparable results to ensemble-based models but with greater flexibility for future sequence/time-series modeling. This pipeline lays the foundation for real-time ETA systems in logistics operations.
