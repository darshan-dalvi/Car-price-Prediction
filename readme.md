# **Car Price Prediction**

This project involves predicting car prices based on various features such as mileage, ownership history, fuel type, and more. The project leverages data preprocessing, feature engineering, and machine learning techniques to deliver an accurate model for price estimation.

## **Table of Contents**
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Features](#features)
4. [Technologies Used](#technologies-used)
5. [Model Performance](#model-performance)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Results](#results)
9. [Future Work](#future-work)

---

## **Overview**
This project aims to:
- Clean and preprocess raw car data.
- Engineer meaningful features to improve model performance.
- Compare and select the best machine learning model.
- Achieve high accuracy and R² scores for predicting car prices.

---

## **Dataset**
The dataset includes key attributes of cars listed for sale:
- **Target Variable**: `Price` (dependent variable)
- **Independent Variables**:
  - Rating
  - City (Encoded)
  - Kilometers Driven
  - Ownership Type
  - Fuel Type
  - Transmission Type
  - Car Age
  - Insurance Validity
  - Engineered Features: `Price_per_Kilometer`, `Normalized_Price`, etc.

---

## **Features**
### Finalized Features for Modeling:
1. `Rating`
2. `City`
3. `Kilometers`
4. `Owner`
5. `Fuel_Type`
6. `Transmission`
7. `Car_Age`
8. `Is_Insurance_Valid`
9. Engineered features like `Price_per_Kilometer`, `Car_Age_Group`.

---

## **Technologies Used**
- **Languages**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost, TensorFlow/Keras
- **Tools**: Jupyter Notebook
- **Deployment**: Model saved using Pickle for future use

---

## **Model Performance**
- **Best Model**: XGBoost
- **Hyperparameter Optimization**: GridSearchCV
- **R² Scores**:
  - Training Data: 0.99
  - Test Data: 0.97

---

## **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/darshan-dalvi/car-price-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd car-price-prediction
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## **Usage**
1. Load the cleaned dataset and model file:
   ```python
   import pickle

   with open('xgboost_model.pkl', 'rb') as file:
       model = pickle.load(file)
   ```
2. Make predictions:
   ```python
   predictions = model.predict(X_test)
   ```

---

## **Results**
- The model successfully predicts car prices with high accuracy, achieving an R² score of 0.97 on test data.
- Important factors influencing price include `Car_Age`, `Transmission`, `Kilometers`, and `Fuel_Type`.

---

## **Future Work**
- Integrate a Flask or FastAPI web app for real-time predictions.
- Include more granular location-based data.
- Add advanced features like car brand or service history.

---

## **Contributing**
Contributions are welcome! Please fork the repository and submit a pull request.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
