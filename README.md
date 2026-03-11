# Machine Failure Prediction Using Machine Learning 🔧

## Project Overview
This project focuses on predicting whether a machine tool will fail during operation using machine learning techniques. Early failure detection helps industries perform predictive maintenance, reduce unexpected downtime, and improve operational efficiency.

The model analyzes machine operational parameters such as temperature, torque, rotational speed, and tool wear to identify patterns that indicate potential failures.

---

## Dataset 📊
The dataset contains machine operational data and sensor readings collected from industrial equipment.

### Features
- Air Temperature  
- Process Temperature  
- Rotational Speed  
- Torque  
- Tool Wear  
- Machine Type  

### Target Variable

**Machine Failure**

| Value | Meaning |
|------|------|
| 0 | Machine Running |
| 1 | Machine Failure|

The dataset is **highly imbalanced**, as failure events occur much less frequently than normal operations.

---

## Methodology ⚙️

### Data Preprocessing
- Removed unnecessary columns (`UDI`, `Product ID`)
- Encoded categorical features using one-hot encoding
- Cleaned feature names for compatibility with the model

### Train-Test Split
The dataset was split into:
- **80% training data**
- **20% testing data**

### Handling Class Imbalance
To improve failure detection, **SMOTE + Tomek Links** were applied:
- SMOTE generates synthetic minority samples
- Tomek Links removes noisy samples near class boundaries

### Model Used
The model used is **XGBoost Classifier**, which is highly effective for structured datasets.
---

## Model Evaluation 📈

The model performance was evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Model Performance

| Metric | Score |
|------|------|
Accuracy | 99% |
Failure Recall | 96% |
Failure Precision | 72% |
F1 Score | 0.82 |

📖 Interpretation
- **High Recall (96%)** → The model detects most machine failures.
- **Precision (72%)** → Most predicted failures are actual failures.

High recall ensures that most machine failures are detected early, which is crucial for predictive maintenance systems.

---

## Technologies Used 💻

- Python  
- Pandas  
- Scikit-learn  
- XGBoost  
- Imbalanced-learn (SMOTE-Tomek)  
- Matplotlib  
- Seaborn  

---

## Project Structure

```
tool-failure-prediction/
│
├── machine_failure.csv
├── predictive_model.ipynb
├── README.md
```

---

## How to Run

Install dependencies:

```bash
pip install pandas scikit-learn xgboost imbalanced-learn seaborn matplotlib
```

Run the notebook:

```
predictive_model.ipynb
```

---

## Applications
- Predictive maintenance  
- Industrial equipment monitoring  
- Manufacturing optimization  
- Failure risk detection  

---

## Author

Levinjoe  
Mechanical Engineer | Data Analytics | Machine Learning
