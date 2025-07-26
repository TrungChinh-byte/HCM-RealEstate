# 🏡 House Price Prediction Using Web Scraping and Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/status-completed-success.svg)

A machine learning project that predicts house prices in Ho Chi Minh City using real-time data scraped from [batdongsan.vn](https://batdongsan.vn). It includes data scraping, data cleaning, EDA, and regression modeling with XGBoost.

## 📂 Table of Contents

- [Demo](#-demo)
- [Features](#-features)
- [Technologies](#-technologies-used)
- [Installation](#-installation)
- [Usage](#-usage)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [License](#-license)
- [Contact](#-contact)

## 🎬 Demo

![Demo GIF](demo/demo.gif)  
*(Replace this with a demo image or GIF of your project)*

---

## ✨ Features

- Scrape real estate listings with `requests + BeautifulSoup`
- Store data in MongoDB Atlas
- Clean and preprocess raw text data
- Perform EDA (visualizations with `matplotlib` and `seaborn`)
- Build and evaluate regression models (XGBoost, Ridge, Linear)
- Save and reuse trained models (`pickle`)

---

## 🛠️ Technologies Used

- Python 3.10
- `requests`, `BeautifulSoup4` for scraping
- `pandas`, `numpy` for data processing
- `matplotlib`, `seaborn` for visualization
- `xgboost`, `scikit-learn` for modeling
- `MongoDB Atlas` for database
- `Jupyter Notebook`

---

## ⚙️ Installation

1. **Clone the repo:**
   ```bash
   git clone https://github.com/yourusername/house-price-prediction.git
   cd house-price-prediction
