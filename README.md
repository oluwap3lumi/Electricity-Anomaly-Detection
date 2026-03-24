# Electricity-Anomaly-Detection
# Context-Aware Electricity Anomaly Detection

##  Overview

Electricity distribution companies face significant revenue losses due to undetected anomalies such as meter tampering, energy theft, and faulty infrastructure.

This project builds an end-to-end machine learning system that:

* Detects anomalous electricity consumption patterns
* Explains *why* anomalies occur using explainable AI (SHAP)
* Predicts future anomalies (early warning system)
* Incorporates weather and temporal context into modeling

---

##  Objectives

* Identify abnormal electricity usage patterns
* Compare supervised and unsupervised anomaly detection methods
* Understand the drivers of anomalies
* Enable decision-making via threshold tuning

---

##  Dataset

The dataset contains:

* Smart meter electricity consumption data
* Weather variables (temperature, humidity, etc.)
* Historical consumption statistics
* Labeled anomalies

---

##  Methodology

### 1. Data Processing

* Timestamp parsing and indexing
* Missing value handling
* Time-series ordering

### 2. Feature Engineering

* Time-based features (hour, day, weekend)
* Lag features (previous consumption values)
* Rolling statistics (mean, standard deviation)
* Consumption dynamics (rate of change, ratios)
* Weather interaction features

---

### 3. Modeling

#### Supervised Learning

* Logistic Regression (baseline)
* Random Forest (primary model)

#### Unsupervised Learning

* Isolation Forest for anomaly detection

---

### 4. Explainability

* SHAP (SHapley Additive Explanations) used to:

  * Identify key drivers of anomalies
  * Explain individual anomaly predictions

---

### 5. Threshold Optimization

* Tuned classification threshold to balance:

  * Precision (reducing false alarms)
  * Recall (capturing more anomalies)

---

### 6. Early Warning System

* Predicts anomalies one step ahead
* Enables proactive intervention

---

##  Results

| Model               | Precision | Recall | F1 Score |
| ------------------- | --------- | ------ | -------- |
| Logistic Regression | XX        | XX     | XX       |
| Random Forest       | XX        | XX     | XX       |
| Isolation Forest    | XX        | XX     | XX       |

> Random Forest achieved the best balance between precision and recall.

---

##  Key Insights

* Sudden consumption spikes and deviations from historical averages are strong anomaly indicators
* Weather variables (especially temperature) significantly influence electricity usage
* Threshold tuning allows alignment with business priorities (risk vs false alarms)

---

##  Explainability Example

SHAP analysis revealed that anomalies are primarily driven by:

* High consumption deviation from rolling averages
* Strong interaction between temperature and consumption
* Abnormal short-term consumption changes

---

##  Sample Visualizations

(Add screenshots here)

* Time series anomaly detection
* Feature importance plots
* SHAP summary plots
* Precision-recall curve

---

##  Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* SHAP
* Matplotlib, Seaborn, Plotly

---

##  How to Run

### 1. Clone repo

```bash
git clone https://github.com/oluwap3lumi/Electricity-Anomaly-Detection.git
cd smart-meter-anomaly-ml
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run notebook

Open the notebook in Google Colab or Jupyter.

---

##  Future Improvements

* Integrate spatial (GIS) features for location-based anomaly detection
* Deploy as a real-time monitoring API
* Build an interactive dashboard for utility operators

