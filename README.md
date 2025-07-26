# 🏡 House Price Prediction Using Web Scraping and Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Notebook](https://img.shields.io/badge/Tool-Jupyter_Notebook-orange.svg)

A machine learning project that predicts house prices in Ho Chi Minh City using real-time data scraped from [batdongsan.vn](https://batdongsan.vn). It includes data scraping, data cleaning, EDA, and regression modeling with XGBoost.

## 📂 Table of Contents

- [Demo](#-demo)
- [Features](#-features)
- [Technologies](#-technologies-used)
- [Results](#-results)
- [Contact](#-contact)

## 🎬 Demo

![Demo GIF](demo/demo.gif)  
<img width="268" height="317" alt="image" src="https://github.com/user-attachments/assets/f3595c89-36e5-4386-9651-3a5994141d2a" />

---

## ✨ Features

- Scrape real estate listings with `requests + BeautifulSoup`
- Store data in MongoDB Atlas
- Clean and preprocess raw text data
- Perform EDA (visualizations with `matplotlib` and `seaborn`)
- Build and evaluate regression models (XGBoost, Ridge, Linear)

### Scrape real estate
- Crawl data from batdongsan.vn, specifically targeting real estate listings in Ho Chi Minh City.

- Step 1: Retrieve all listing URLs from the main page of batdongsan.vn/ho-chi-minh.

- Step 2: For each listing URL, extract detailed information including:

    - Price, area, number of bedrooms, bathrooms, description, etc.
    - Location data: district, ward, address
    - Seller information (name, phone, ...)

- Step 3: Structure the extracted data into a JSON array format.

- Step 4: Save the raw data into MongoDB Atlas for further analysis and reuse.

### Clean and preprocess raw text data
- Load raw data from MongoDB Atlas for preprocessing.

- Convert unstructured data into clean, rectangular tabular format suitable for analysis and modeling.

- Remove redundant symbols and units (e.g., "Area: 27m²" → 27).

- Extract additional features such as the number of floors by parsing the textual description field using regex.

- Handle missing values, especially in critical fields like number of floor and area.

### Perform EDA
- Use histograms and boxplots to visualize data distribution and detect potential outliers in numerical features such as price, area, and number of floors.

- Use bar charts to analyze categorical insights, including:

  - The most expensive districts (based on average price)

  - The most active sellers (based on number of listings posted)

  - The most active districts (based on total number of listings)


### Build and evaluate regression models
- Build machine learning models to estimate house prices based on extracted features:

- Train and compare three different regression algorithms:
  - Ridge Regression
  - RandomForest
  - XGBoost Regressor

- Evaluate models using metrics like MSE and R² Score on the test set.

- Choose XGBoost as the best-performing model for house price prediction due to its performance and ability to handle non-linear relationships.

---
## 🛠️ Technologies

- Python 3.10, Jupyter Notebook
- `requests`, `BeautifulSoup4` for scraping
- `pandas`, `numpy` for data processing
- `matplotlib`, `seaborn` for visualization
- `xgboost`, `scikit-learn` for modeling
- `MongoDB Atlas` for database

---

## 📈 Results

- Best model: XGBoost

- MSE on test set: 2.82 Billion VND

- R² Score: 0.53


