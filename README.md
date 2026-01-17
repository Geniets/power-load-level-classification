# Power Load Classification

## Project Overview
This project focuses on building a machine learning model to **predict the Load Type of a power system** based on historical energy consumption and electrical parameters. The task is framed as a **multi-class classification problem**, where the target variable (`Load_Type`) can take one of the following values:

- Light_Load  
- Medium_Load  
- Maximum_Load  

The project was completed as part of an **AI/ML internship assignment** and demonstrates an end-to-end machine learning workflow.

---

## Objective
The primary objective is to develop a classification model that accurately predicts the **Load_Type** using historical power system data, while following a realistic validation strategy and appropriate evaluation metrics.

---

## Dataset Description
The dataset contains monthly power system observations with the following features:

| Feature | Description |
|-------|-------------|
| Date | Continuous time data (first day of each month) |
| Usage_kWh | Industry energy consumption (kWh) |
| Lagging_Current_Reactive_Power | Reactive power (kVarh) |
| Leading_Current_Reactive_Power | Reactive power (kVarh) |
| CO2 | Carbon dioxide emissions (ppm) |
| NSM | Number of seconds from midnight |
| Load_Type | Target variable (Light, Medium, Maximum Load) |

---

## Data Availability
The dataset used in this project was provided as part of the assignment and is **not included in this repository due to data confidentiality constraints**.

The notebook assumes the dataset is available locally in CSV format and demonstrates the complete preprocessing, training, and evaluation workflow.

---

## Approach
The project follows a structured machine learning pipeline:

1. **Data Preprocessing**
   - Feature selection
   - Handling categorical variables
   - Time-based train-test split

2. **Exploratory Data Analysis (EDA)**
   - Distribution analysis
   - Feature relationships with the target variable

3. **Model Selection and Training**
   - A **Random Forest Classifier** was selected for its robustness and ability to handle non-linear relationships
   - Hyperparameter tuning performed using **GridSearchCV**

4. **Validation Strategy**
   - The **last month of data** was held out as the test set to simulate real-world prediction on unseen data

5. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - F1-score

---

## Model Used
- **Random Forest Classifier** (scikit-learn)
- A single finalized model trained after hyperparameter tuning

---

## Results
The trained model demonstrates strong performance across all classification metrics on the unseen test set, indicating good generalization capability on recent data.

---

## Repository Structure
