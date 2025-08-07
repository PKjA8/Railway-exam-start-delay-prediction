# 🚆 Arrival to Exam Start Time Prediction – Indian Railways

A machine learning project to predict the delay between a train rake's **arrival** and the **start of its safety examination** in Indian Railways yards. This helps in optimizing yard operations, improving turnaround time, and enabling data-driven manpower planning.



## 📌 Problem Statement

In Indian Railways, each train rake (group of wagons/coaches) must undergo a mandatory safety exam upon arrival. However, delays often occur between arrival and examination start due to:
- Yard congestion
- Staff shortages
- Poor scheduling and planning

This delay is termed as **"Arrival to Exam Start Time" (`ar_to_ex_st`)**.



## 🎯 Project Objectives

- Predict `ar_to_ex_st` delay using historical data and ML models.
- Improve yard management by enabling early delay estimation.
- Reduce idle time and optimize manpower deployment.
- Support smarter, data-driven railway operations.

---

## 🧠 Methodology

### 1. **Data Source**
- Real operational data from **CRIS (Centre for Railway Information Systems)**.
- Over **5.8 lakh records** (Dec 2022 – July 2025).

### 2. **Data Cleaning & Preprocessing**
- Dropped invalid/outlier records using **yard-wise IQR method**.
- Removed 2022 data due to inconsistencies.
- Feature engineering: congestion level, rake type, weekday, hour of arrival, etc.
- Final cleaned dataset: ~3.35 lakh rows.

### 3. **Modeling Approach**
- Applied regression algorithms: `XGBoost`, `RandomForest`, `LightGBM`, `CatBoost`, `Stacking`.
- Target variable: `ar_to_ex_st` (in minutes).
- Categorical encoding: **Guided Ordinal Encoding** based on target mean.

### 4. **Evaluation Metrics**
- **MAE** (Mean Absolute Error)
- **R² Score**

| Model               | MAE (min) | R² Score |
|--------------------|-----------|----------|
| XGBoost            | 77.45     | 0.6245   |
| Random Forest      | 82.93     | 0.5644   |
| LightGBM           | 87.83     | 0.5291   |
| CatBoost           | 84.51     | 0.4309   |
| Stacking Regressor | 93.26     | 0.5126   |

---

## 📊 Key Insights from EDA

- **Yard ID** is the most important predictor of delay.
- Delay patterns vary across **weekdays**, **months**, and **rake types**.
- Certain **BPC categories** take much longer to examine.
- **Wednesday** shows the highest average delay, **Thursday** the least.

---

## 🔧 Tools & Technologies Used

- `Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn`
- `XGBoost` · `LightGBM` · `CatBoost` · `Scikit-learn`
- `Jupyter Notebook` · `VS Code`

---

## 🚀 Outcomes & Future Scope

### ✅ Operational Benefits
- Predict delay **before rake arrival** – improves yard planning.
- Enables **dynamic resource allocation** and **bottleneck avoidance**.
- Supports integration with **CRIS dashboards** for real-time monitoring.

### 🔄 Future Scope
- Integrate with real-time systems like **FOIS**.
- Add contextual features: staff availability, weather, shift details.
- Deploy as a **web/mobile dashboard** for yard supervisors.
- Extend to predict: exam completion time, dispatch time, full cycle delay.

---

## 👥 Authors

- **Harphool Singh** (23AI023)  
- **Pradeep Kumar** (23AI038)  
B.Tech – Artificial Intelligence & Data Science  
Gati Shakti Vishwavidyalaya, Ministry of Railways, Vadodara

---

## 📄 License

This project is part of an academic internship and is intended for educational and research purposes. For any use in production or integration with official railway systems, proper authorization from CRIS is required.

---

## 📬 Contact

For queries, suggestions, or collaboration opportunities:
📧 pradeep.kumar@xyz.edu | 📧 harphool.singh@xyz.edu  
📍 Gati Shakti Vishwavidyalaya, Vadodara, India

