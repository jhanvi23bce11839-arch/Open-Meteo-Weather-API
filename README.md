# Weather Classification using SVM and Open-Meteo API

## Objective

The objective of this project is to classify weather conditions as **Warm** or **Cool** using meteorological data obtained from the Open-Meteo Weather API. A Support Vector Machine (SVM) classifier with an RBF kernel is trained to predict the weather class based on weather parameters.

---

## Dataset / Data Source

This project uses real-time weather forecast data from the Open-Meteo API.

**API Documentation:**  
https://open-meteo.com/

**Example API Endpoint:**
https://api.open-meteo.com/v1/forecast

The dataset is fetched dynamically at runtime; no CSV dataset is required.

---

## Features Used

- Temperature
- Relative Humidity
- Surface Pressure
- Wind Speed

### Target Variable

**Weather_Class**

- Warm → Temperature ≥ 25°C
- Cool → Temperature < 25°C

---

## Libraries Used

- requests
- pandas
- scikit-learn
- matplotlib
- seaborn

---

## Methodology

1. Fetch weather data from the Open-Meteo API.
2. Convert the JSON response into a Pandas DataFrame.
3. Create the target variable (Weather_Class) based on temperature.
4. Check for missing values and preprocess the dataset.
5. Encode the target labels.
6. Split the data into 80% training and 20% testing sets.
7. Standardize the feature values using StandardScaler.
8. Train an SVM Classifier using the RBF kernel.
9. Predict weather classes for the test dataset.
10. Evaluate the model using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.

---

## Results

| Metric | Value |
|--------|-------|
| Accuracy | 97.06% |
| Precision | 100.00% |
| Recall | 75.00% |
| F1-Score | 85.71% |

The model achieved high classification accuracy and demonstrated strong performance in distinguishing between Warm and Cool weather conditions.

---

## Conclusion

The SVM classifier successfully classified weather conditions using meteorological features obtained from the Open-Meteo API. The model achieved an accuracy of **97.06%**, demonstrating excellent overall performance. Feature scaling using **StandardScaler** significantly improved the classifier's effectiveness, as SVM is sensitive to differences in feature scales. The RBF kernel enabled the model to capture non-linear relationships between weather parameters. While SVM provides high prediction accuracy, its performance may be affected by class imbalance and parameter selection. Overall, this project demonstrates the effectiveness of SVM for weather classification using real-time weather data.

---

## Author

**Jhanvi Nair**
