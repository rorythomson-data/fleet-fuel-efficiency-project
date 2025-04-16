# Fleet Fuel Efficiency Project 🚛⛽

This project is part of my preparation for a Datathon hosted by ZF SCALAR, focused on analyzing truck fleet telemetry data. I'm using this project to practice EDA, feature engineering, clustering, supervised modeling, and Git version control — all using a dataset that simulates GPS, speed, idling, and fuel usage across 7,500 trips.

I recently completed a Data Science bootcamp and am transitioning into the field after years of experience as a language teacher. This project is also helping me build up my GitHub portfolio and prepare for my first internship, which starts in May.

---

## 🗂 Dataset

The dataset is synthetic but modeled on realistic fleet telemetry. It contains ~7,500 trip records with:
- `vehicle_id`, `driver_id`, `route_type` (urban/rural/mixed)
- `start_time`, `end_time`, `trip_day_of_week`
- `distance_km`, `avg_speed_kmph`, `idle_time_min`
- `fuel_consumed_liters` (target variable)

---

## 🎯 Project Goals

- Perform exploratory data analysis (EDA)
- Visualize key relationships (e.g., speed vs fuel, route vs efficiency)
- Engineer meaningful features (e.g., trip duration, efficiency ratios)
- Cluster driving patterns to identify inefficient behavior
- Build a regression model to predict fuel usage
- Practice clear documentation and Git versioning

---

## 🔁 Workflow

1. **EDA** – Understand data structure, patterns, and outliers
2. **Visualization** – Use seaborn/matplotlib to communicate insights
3. **Feature Engineering** – Create new columns to improve modeling
4. **Clustering** – Use K-Means to group trips by behavior
5. **Regression Modeling** – Predict fuel consumption
6. **Evaluation** – Use MAE, RMSE, and R² to assess performance
7. **Git Integration** – Commit and push progress incrementally

---

## ▶️ How to Run

1. Clone the repo  
2. Open the notebook inside `/notebooks/`  
3. Run from top to bottom in Jupyter or VS Code  
4. Dataset is located in `/data/`

---

## 📊 Outputs (in progress)

- [ ] Initial EDA visuals
- [ ] Cluster plot by route type
- [ ] Regression performance metrics
- [ ] Feature importance chart

---

## 📌 Next Steps

- Clean and polish clustering notebook
- Try a second regression model (e.g., Random Forest)
- Build a dashboard or visual summary
- Prep insights slide for Datathon

---

## 🙏 Acknowledgements

Inspired by projects from [365 Data Science](https://www.udemy.com/course/the-data-science-course-complete-data-science-bootcamp/) and supported by my ongoing self-study and bootcamp work at Nuclio School.
