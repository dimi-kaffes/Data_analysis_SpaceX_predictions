# 🚀 SpaceX Falcon 9 First-Stage Landing Prediction

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Framework](https://img.shields.io/badge/Framework-Scikit--Learn%20%7C%20Dash-orange)](https://scikit-learn.org/)

An end-to-end data science and machine learning project predicting whether the first stage of SpaceX's Falcon 9 rocket will land successfully. By forecasting booster reusability, this project helps evaluate the cost efficiency of orbital rocket launches.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features & Highlights](#-key-features--highlights)
- [Project Architecture](#-project-architecture)

---

## 💡 Project Overview

SpaceX advertises Falcon 9 rocket launches on its website with a baseline cost of **$62 million**, whereas other providers cost upward of **$165 million** each. Much of these savings stem from SpaceX’s ability to successfully land and reuse the rocket's first stage booster. 

This project analyzes historical launch records to predict first-stage landing outcomes (Land vs. Crash/Ocean Ditch) using machine learning classification models.

---

## 🎯 Key Features & Highlights
* **Automated Data Pipeline:** Extracted launch telemetry directly from the **SpaceX REST API** and web-scraped historical launch records from Wikipedia using **BeautifulSoup**.
* **Relational EDA:** Executed SQL queries to evaluate payload distributions, site-specific launch success, and booster flight counts.
* **Geospatial Analytics:** Rendered interactive launch site maps, proximity clusters, and landing trajectories with **Folium**.
* **Machine Learning Pipeline:** Evaluated multiple classification models (Logistic Regression, SVM, Decision Tree, KNN) tuned via `GridSearchCV`.
* **Interactive Dashboard:** Built a live analytics app using **Plotly Dash** featuring interactive payload sliders and launch site dropdowns.

---

## 🏗️ Project Architecture

```mermaid
graph LR
    A[SpaceX API / Wikipedia] --> B[Data Wrangling & Cleaning]
    B --> C[EDA via SQL & Seaborn]
    C --> D[Geospatial Mapping - Folium]
    C --> E[ML Modeling & Tuning]
    D --> F[Interactive Dashboard - Dash]
    E --> F
