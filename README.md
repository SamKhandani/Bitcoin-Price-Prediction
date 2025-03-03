# پیش‌بینی قیمت بیت‌کوین با استفاده از مدل LSTM چندلایه  
**Bitcoin Price Prediction Using a Multi-Layer LSTM Model**

[![TensorFlow Badge](https://img.shields.io/badge/TensorFlow-2.0%2B-FF6F00?logo=TensorFlow&logoColor=white)](https://www.tensorflow.org/)
[![Keras Badge](https://img.shields.io/badge/Keras-2.0%2B-D00000?logo=Keras&logoColor=white)](https://keras.io/)
[![Scikit-learn Badge](https://img.shields.io/badge/Scikit--learn-1.0%2B-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![Python Badge](https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=Python&logoColor=white)](https://www.python.org/)

---

## فهرست مطالب (فارسی)
1. [مقدمه](#مقدمه)
2. [ویژگی‌های اصلی پروژه](#ویژگی‌های-اصلی-پروژه)
3. [پیش‌نیازها](#پیش‌نیازها)
4. [نحوه اجرا](#نحوه-اجرا)
5. [توضیحات کد](#توضیحات-کد)
6. [نتایج و نمودارها](#نتایج-و-نمودارها)
7. [بهبود و سفارشی‌سازی](#بهبود-و-سفارشیسازی)
8. [لایسنس](#لایسنس)

---

## Table of Contents (English)
1. [Introduction](#introduction)
2. [Key Features](#key-features)
3. [Prerequisites](#prerequisites)
4. [How to Run](#how-to-run)
5. [Code Explanation](#code-explanation)
6. [Results and Plots](#results-and-plots)
7. [Improvements & Customization](#improvements--customization)
8. [License](#license)

---

## مقدمه
این مخزن شامل یک مدل **LSTM** چندلایه دوطرفه (Bidirectional) برای پیش‌بینی قیمت بیت‌کوین است. داده‌ها شامل ویژگی‌های قیمتی (`Open`, `High`, `Low`, `Close`, `Volume`) و اندیکاتورهای تکنیکال (RSI، MACD، Moving Averages و غیره) می‌باشند. هدف این است که بر اساس داده‌های گذشته، مقدار **High**، **Low** و **Close** روز بعد را پیش‌بینی کنیم.

---

## Introduction
This repository contains a **Bidirectional Multi-Layer LSTM** model to predict Bitcoin prices. The dataset includes price features (`Open`, `High`, `Low`, `Close`, `Volume`) along with technical indicators (RSI, MACD, Moving Averages, etc.). The goal is to forecast the **High**, **Low**, and **Close** for the next day based on historical data.

---

## ویژگی‌های اصلی پروژه
- استفاده از **Bidirectional LSTM** در سه لایه برای یادگیری بهتر توالی‌های زمانی.
- استفاده از **Regularization (L2)** و **Dropout** برای کاهش **Overfitting**.
- **Batch Normalization** جهت بهبود پایداری و سرعت آموزش.
- استفاده از **اندیکاتورهای تکنیکال** مهم مانند RSI, MACD, MA-20, MA-50, MA-200 و غیره.
- آموزش مدل با **Adam** و تنظیم **Learning Rate** مناسب (`0.0005`).
- استفاده از **EarlyStopping** و **ReduceLROnPlateau** برای جلوگیری از بیش‌برازش و تنظیم پویای نرخ یادگیری.
- ارزیابی با **MAE**, **RMSE**, **R²** و **MAPE**.

---

## Key Features
- Three-layer **Bidirectional LSTM** architecture for improved sequence learning.
- **Regularization (L2)** and **Dropout** to reduce **Overfitting**.
- **Batch Normalization** to stabilize and accelerate training.
- Incorporation of critical **Technical Indicators** such as RSI, MACD, MA-20, MA-50, MA-200, etc.
- Model training with **Adam** optimizer at a tuned **Learning Rate** (`0.0005`).
- **EarlyStopping** and **ReduceLROnPlateau** to avoid overfitting and dynamically adjust the learning rate.
- Performance evaluation using **MAE**, **RMSE**, **R²**, and **MAPE**.

---

## پیش‌نیازها
برای اجرای این پروژه نیاز به نصب کتابخانه‌های زیر دارید:
- [Python](https://www.python.org/) >= 3.8  
- [TensorFlow](https://www.tensorflow.org/) >= 2.0  
- [Keras](https://keras.io/) (در نسخه‌های جدید TensorFlow، Keras به صورت توکار موجود است)  
- [Numpy](https://numpy.org/)  
- [Pandas](https://pandas.pydata.org/)  
- [Matplotlib](https://matplotlib.org/)  
- [Plotly](https://plotly.com/)  
- [scikit-learn](https://scikit-learn.org/stable/)

برای نصب سریع، می‌توانید از دستور زیر استفاده کنید:
```bash
pip install tensorflow keras numpy pandas matplotlib plotly scikit-learn
```
