# Diabetes Detection with Machine Learning

## Objective

This project aims to develop and compare machine learning models to predict the presence of diabetes based on clinical and demographic data.

The main focus is **maximizing recall for the positive class** (diabetes diagnosis), ensuring that as many cases as possible are identified, while maintaining the model’s overall performance.

---

## Data Used

* **Variables**:

  * `HbA1c_Level` — average blood glucose level over the past 3 months
  * `Blood_Glucose_Level` — glucose measured at the moment
  * `Age` — patient’s age
  * `BMI` — body mass index
  * `Hypertension`, `Heart_Disease` — binary indicators
  * `Gender` — male/female
  * `Smoking_History` — yes/no

---

## Methodology

1. **Preprocessing**:

   * Handling missing values
   * Encoding categorical variables
   * Dataset balancing using `scale_pos_weight`

2. **Models tested**:

   * **XGBoost**
   * **Random Forest**
   * **Neural Network (Keras/TensorFlow)**

3. **Evaluation metrics**:

   * `Precision`, `Recall`, `F1-score`
   * `ROC AUC`
   * Confusion matrix
   * Feature importance (for tree-based models)

## 📊 Results

### 🔹 XGBoost

<img width="457" height="218" alt="image" src="https://github.com/user-attachments/assets/129fdc94-191e-4eee-b182-acfc09f36ae2" />


### 🔹 Random Forest

<img width="457" height="218" alt="image" src="https://github.com/user-attachments/assets/50816b22-6d5f-4f3f-933c-fa9dfe8fc632" />

---


## 📈 Overall Comparison

* Both models achieved an **AUC ROC above 0.97**.
* **XGBoost** showed **better recall** for the positive class (diabetes identification).
* **Random Forest** performed similarly, but with slightly lower recall.

