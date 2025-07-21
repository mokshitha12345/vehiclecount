# Vehicle Count Prediction Using Random Forest Regressor

## 📄 Project Overview

This project focuses on **predicting vehicle counts** from timestamp data using a **Random Forest Regression model**. The dataset consists of hourly vehicle counts, and various time-based features are extracted from the `DateTime` column to improve prediction accuracy.

The workflow includes:

- **Data Loading and Preprocessing**
- **Feature Extraction from `DateTime`**
- **Model Training using RandomForestRegressor**
- **Prediction and Visualization**
- **Saving Output Plot**

---

## 📂 Dataset

**Input File**: `vehicles.csv`

### Columns:

| Column Name | Description                      |
|-------------|----------------------------------|
| DateTime    | Timestamp (hourly intervals)    |
| Vehicles    | Number of vehicles observed      |

---

## ⚙️ Feature Engineering

The following features are extracted from `DateTime`:

| Feature Name | Description                     |
|--------------|---------------------------------|
| date         | Day of the month (1–31)         |
| weekday      | Day of the week (0=Monday, 6=Sunday) |
| hour         | Hour of the day (0–23)          |
| month        | Month number (1–12)             |
| year         | Year (e.g., 2015)               |
| dayofyear    | Day of the year (1–365/366)     |
| weekofyear   | Week number in the year         |

After extraction, the original `DateTime` column is dropped.

---

## 🧰 Requirements

Install the necessary Python libraries:

```bash
pip install pandas scikit-learn matplotlib
