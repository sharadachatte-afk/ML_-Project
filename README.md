# 🚗 Ford Car Price Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting the **price of Ford cars** using Machine Learning techniques. The dataset contains information about Ford vehicles, including their model, year, mileage, tax, MPG, engine size, transmission, and fuel type.

The project performs **Exploratory Data Analysis (EDA)**, data preprocessing, categorical encoding, feature scaling, and **Linear Regression** to predict car prices.

## 📂 Dataset

The dataset used in this project is the **Ford Car Price Prediction dataset**.

The dataset contains information about different Ford car models and their prices.

### Important Features

* `model` – Ford car model
* `year` – Manufacturing year
* `price` – Price of the car (Target Variable)
* `transmission` – Type of transmission
* `mileage` – Distance travelled by the car
* `fuelType` – Type of fuel
* `tax` – Vehicle tax
* `mpg` – Miles per gallon
* `engineSize` – Engine size

## 🎯 Objectives

The main objectives of this project are:

* Understand the Ford car dataset.
* Perform Exploratory Data Analysis.
* Identify relationships between car features and price.
* Handle categorical variables.
* Convert categorical data into numerical form.
* Scale numerical features.
* Split the dataset into training and testing sets.
* Build a Linear Regression model.
* Predict Ford car prices.
* Evaluate the model using the **R² Score** and **Adjusted R² Score**.

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Kaggle Notebook / Jupyter Notebook

## 🔍 Exploratory Data Analysis

The project performs several EDA techniques to understand the dataset.

### Data Inspection

The following operations are performed:

```python
df.head()
df.shape
df.isnull().sum()
df.columns
```

These operations help understand the dataset structure, number of records, columns, and missing values.

### Data Visualization

Different plots are used to analyze the relationship between car features and price:

* Histogram of car prices
* Correlation heatmap
* Box plot of year vs. price
* Scatter plot of mileage vs. price
* Box plot of transmission vs. price
* Box plot of fuel type vs. price
* Box plot of car model vs. price

These visualizations help identify trends, relationships, and possible outliers.

## 🔄 Data Preprocessing

### Categorical Encoding

Categorical features such as:

* `model`
* `transmission`
* `fuelType`

are converted into numerical values.

Two encoding approaches are explored:

### One-Hot Encoding

```python
pd.get_dummies()
```

### Label Encoding

```python
LabelEncoder()
```

This allows categorical information to be used by Machine Learning algorithms.

## 📏 Feature Scaling

`StandardScaler` is used to standardize numerical features.

The selected numerical features include:

```text
year
tax
mpg
engineSize
```

Feature scaling helps put numerical variables on a comparable scale.

## 🤖 Machine Learning Model

### Linear Regression

The main Machine Learning algorithm used in this project is **Linear Regression**.

The target variable is:

```text
price
```

The remaining features are used as independent variables to predict the price of a Ford car.

The dataset is divided into:

* **67% Training Data**
* **33% Testing Data**

using `train_test_split()`.

## 📊 Model Evaluation

The model is evaluated using:

### R² Score

R² Score measures how well the independent variables explain the variation in the target variable.

```python
r2 = r2_score(y_test, y_pred)
```

### Adjusted R² Score

Adjusted R² takes the number of predictors into account and provides a more adjusted measure of model performance.

The formula used is:

```python
adjusted_r2 = 1 - ((1-r2) * (n-1) / (n-p-1))
```

where:

* `R²` = R-squared score
* `n` = Number of observations
* `p` = Number of predictors

## 📈 Prediction

After training the Linear Regression model, predictions are generated using:

```python
y_pred = model.predict(x_test)
```

The predicted prices are then compared with the actual prices using the evaluation metrics.

## 📁 Project Structure

```text
Ford-Car-Price-Prediction/
│
├── ford_car_price_prediction.ipynb
├── README.md
├── requirements.txt
└── dataset/
    └── ford.csv
```

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 3. Open the Notebook

Open:

```text
ford_car_price_prediction.ipynb
```

using Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

### 4. Run the Cells

Run the notebook cells in order to:

1. Load the dataset
2. Perform EDA
3. Encode categorical features
4. Scale numerical features
5. Split the data
6. Train the Linear Regression model
7. Predict car prices
8. Calculate R² and Adjusted R²

## ⚠️ Note

This project is a **Supervised Machine Learning project**, specifically a **Regression problem**, because the `price` column is used as the target variable.

The code also explores different preprocessing techniques such as One-Hot Encoding and Label Encoding.

## 🔮 Future Improvements

The project can be improved by:

* Trying Random Forest Regression
* Trying Decision Tree Regression
* Trying Gradient Boosting
* Comparing multiple regression algorithms
* Performing hyperparameter tuning
* Removing or analyzing outliers
* Using cross-validation
* Adding actual vs. predicted price visualization
* Deploying the model using Streamlit

## 🏁 Conclusion

This project demonstrates a complete Machine Learning workflow for **Ford car price prediction**.

The workflow includes data loading, data cleaning, exploratory data analysis, categorical encoding, feature scaling, model training, prediction, and model evaluation.

The **Linear Regression** model is used to learn the relationship between Ford car features and their prices and can be evaluated using **R² and Adjusted R² scores**.

## 👩‍💻 Author

**Sharda Chatte**

---

⭐ If you found this project useful, consider giving the repository a star!
