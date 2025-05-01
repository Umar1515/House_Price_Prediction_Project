# House_Price_Prediction_Project
Regression Project for Predicting House Prices Using Machine Learning 

# 🏠 House Price Prediction using Machine Learning & Deep Learning

This repository presents a comprehensive analysis and modeling pipeline for predicting house sale prices using the **Ames Housing Dataset**. It includes preprocessing, feature selection, and model comparisons between **Linear Regression**, **Random Forest**, and a **Neural Network**.

## 📊 Dataset

- **Source**: AmesHousing.csv (Ames, Iowa)
- **Size**: 2,930 entries, 82 features (before cleaning)
- **Target Variable**: `SalePrice`

## 🔍 Features & Cleaning

- Dropped columns with >40% missing values.
- Imputed numeric values using **median** and categorical with **mode**.
- Used **Label Encoding** for categorical features.
- Selected top 10 predictive features using:
  - Pearson Correlation
  - ANOVA F-test

## 🔧 Feature Selection (Top 10)
- Overall Qual
- Gr Liv Area
- Garage Cars
- Exter Qual
- Total Bsmt SF
- 1st Flr SF
- Bsmt Qual
- Kitchen Qual
- Garage Area
- Year Built

## 🧪 Models Used

### 1. Linear Regression
- Baseline performance.
- Scaled features with `StandardScaler`.

### 2. Random Forest Regressor (Tuned)
- Tuned using `RandomizedSearchCV`.
- Parameters: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`.

### 3. Artificial Neural Network (ANN)
- Built using **TensorFlow/Keras**:
  - Layers: [256 → 128 → 64 → 32 → 16 → 1]
  - Dropout Regularization
  - Optimizer: Adam
  - Loss: Mean Squared Error (MSE)
  - EarlyStopping used to prevent overfitting

## 📈 Model Evaluation

| Model              | R² Score | MAE       | RMSE      |
|-------------------|----------|-----------|-----------|
| Linear Regression | 0.832    | 23,320    | 36,737    |
| Random Forest      | 0.876    | 18,439    | 31,561    |
| Neural Network     | 0.856    | 20,814    | 34,027    |

## 📉 Visualizations
- Feature correlations
- Boxplots and scatter plots of important features
- Predicted vs Actual price scatterplots
- Loss curves for ANN

## 📁 Project Structure

House_Price_Prediction_Project/ ├── House_Price_Prediction.ipynb # Main notebook with code and outputs ├── AmesHousing.csv # Raw dataset ├── README.md # Project documentation

markdown
Copy
Edit

## 🧠 Conclusions

- **Random Forest** outperformed other models with the highest accuracy.
- **Neural Network** gave competitive results but required more training time.
- **Feature selection** significantly boosted performance by focusing only on relevant predictors.

## 🚀 Future Improvements

- Try ensemble stacking of models
- Tune Neural Network hyperparameters
- Use cross-validation for deep learning model evaluation

## 👤 Author

**Umar1515**  
[🔗 GitHub Repo](https://github.com/Umar1515/House_Price_Prediction_Project)

---
