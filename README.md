# 📈 Linear Regression on Synthetic Dataset (Noise Analysis Included)

## 📌 Project Overview

This project demonstrates the implementation and evaluation of **Simple Linear Regression** using a synthetically generated dataset.

Instead of using a real-world dataset, the data was generated using a known linear relationship:

Y = 4.5X + Noise

This allows validation of the model against a known ground truth.

---

## 🎯 Objective

* Understand how Linear Regression behaves under controlled noise.
* Analyze residual distribution.
* Compare performance under different noise levels.
* Validate whether the model recovers the true slope parameter.

---

## 🛠️ Tech Stack

* Python
* NumPy
* Matplotlib
* Scikit-learn

---

## 📊 Data Generation

Two experiments were conducted:

### 1️⃣ High Noise Scenario

```python
X = np.random.rand(50,1) * 100
Y = X*4.5 + np.random.randn(50,1) * 20
```

* Standard deviation of noise = 20
* Result: Wider residual spread and lower R²

### 2️⃣ Low Noise Scenario

```python
X = np.random.rand(50,1) * 100
Y = X*4.5 + np.random.randn(50,1) * 5
```

* Standard deviation of noise = 5
* Result: Tighter residual distribution and higher R²

---

## 📈 Model Training

* Data split into training and testing sets
* Linear Regression model fitted using Ordinary Least Squares (OLS)
* Predictions generated on test set

---

## 📉 Evaluation & Analysis

### ✅ Actual vs Predicted Plot

* Points align closely with 45° line
* Indicates strong model performance

### ✅ Residual Plot

* Residuals scattered randomly around zero
* No visible curvature
* No strong heteroscedasticity
* Confirms correct model specification

### ✅ Error Distribution

* Residuals approximately normally distributed
* Spread matches theoretical noise variance
* Larger noise → wider distribution

### ✅ Metrics Used

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

---

## 🔬 Key Observations

* The model successfully recovered the true slope (≈ 4.5).
* Lower noise resulted in:

  * Higher R²
  * Smaller residual variance
  * More stable coefficient estimates
* Increasing dataset size improves coefficient stability (Law of Large Numbers).

---

## 🧠 Concepts Practiced

* Data generating process
* Signal-to-noise ratio
* Residual analysis
* Bias–variance understanding
* Model validation against known parameters

---

## 🔗 Kaggle Notebook

You can view the complete implementation and outputs on Kaggle:

👉 [View Notebook on Kaggle](https://www.kaggle.com/code/deveshjangid01/linear-regression)
---

## 📌 Future Improvements

* Increase dataset size to analyze parameter convergence.
* Add Multiple Linear Regression.
* Introduce non-linear data to demonstrate model misspecification.
* Compare with Polynomial Regression.

---

## 🤝 About Me

I am currently practicing Machine Learning fundamentals with a focus on building strong conceptual clarity and internship-ready skills in AI/ML.

---

This version shows:

* Conceptual depth
* Mathematical awareness
* Proper evaluation thinking

If you want, I can now give you an even stronger version that sounds like a mini research experiment instead of a beginner project.
