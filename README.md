#  Uber Ride Data Analysis & Machine Learning Model Comparison  
### **Analyzing Ride Patterns and Customer Behavior in Uber**

---

##  Project Overview
This project performs a full Data Science workflow on an Uber ride dataset to understand customer behavior, ride patterns, trip characteristics, and distance profiles.  

We explore the dataset through **Exploratory Data Analysis (EDA)**, perform **hypothesis testing**, and develop and compare **two machine learning models** to predict trip distance (Miles).  
Although the prediction task is challenging due to limited features, the comparison provides insights into model behavior and feature effectiveness.

---

The dataset contains anonymized Uber ride information with the following key attributes:

| Column | Description |
|--------|-------------|
| CATEGORY | Business or Personal ride |
| PURPOSE | Reason for ride (Meetings, Meals, etc.) |
| START_DATE | Timestamp of the trip |
| MILES | Total distance of the trip |
| TRIP_DURATION | Trip duration in minutes |
| HOUR, DAY, MONTH | Extracted time-based features |
| SPEED | Calculated (Miles / Hour) |

### Data Source Justification
The dataset used here is an educational Uber-style dataset, designed to replicate real ride patterns.  
Although it is not from Uber's internal systems, it follows real-world structure, allowing complete data science analysis including:

- Data preprocessing  
- Feature engineering  
- Visualization  
- Hypothesis testing  
- Model building and comparison  

This makes the dataset suitable for academic learning and project demonstration.

---

##  Data Preprocessing Steps
The following steps were performed:

✔ Handling missing values  
✔ Removing duplicates  
✔ Fixing invalid and unrealistic values  
✔ Normalizing speed values  
✔ Removing outliers (3-sigma rule)  
✔ Creating new engineered features  
✔ Label Encoding of categorical data  

---

## Feature Engineering
To enrich the dataset and improve model capability, the following features were created:

- **SPEED** → Miles divided by duration  
- **day_to_night** → Day or Night ride  
- **IS_RUSH_HOUR** → 7–9 AM and 5–7 PM  
- **IS_WEEKEND** → Saturday / Sunday  
- **DISTANCE_TYPE** → Short / Medium / Long  
- **SPEED_CATEGORY** → Slow / Normal / Fast  
- **MILES_PER_MIN** → Ride intensity  

These engineered features help uncover deeper patterns and improve model interpretation.

---

##  Exploratory Data Analysis (EDA)

EDA covers:

- Most common ride categories  
- Top ride purposes  
- Distribution of miles  
- Peak ride hours  
- Day vs night ride comparison  
- Monthly ride trends  
- Boxplots for outlier detection  
- Speed analysis  
- Hour-wise behavior  

All visualizations are saved automatically in the folder:  
 `outputfile/`

---

## Hypothesis Testing
We performed a **Two-Sample t-Test** to compare:

### **H0:**  
There is no significant difference between the miles of Day and Night rides.

### **Conclusion:**  
Based on the p-value, we examined whether day and night rides differ in distance.  
(Final result will appear when running the code.)

---

## Machine Learning Models

Two ML models were trained to predict ride distance (Miles):

### **Model 1 → Linear Regression**  
Simple baseline model.

### **Model 2 → Random Forest Regressor**  
Advanced non-linear model.

###  Model Comparison Includes:
- R² Accuracy Score  
- Error curves  
- Actual vs Predicted visualization  
- Interpretation of model behavior  

Both models showed low accuracy since the dataset lacks GPS locations, traffic data, and route information—essential for predicting trip distance.  
This limitation is discussed clearly in the conclusion.

---

##  Key Insights
- Business rides dominate the dataset.  
- Most trips happen during morning and evening rush hours.  
- Weekdays show higher ride counts than weekends.  
- Purpose-based analysis shows Meetings and Meals dominate business travel.  
- ML models perform poorly due to lack of spatial and route features.

---

##  Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- SciPy  
- Jupyter Notebook  

---

##  Project Folder Structure

