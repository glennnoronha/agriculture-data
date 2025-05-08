# 🌾 Crop Yield Prediction with Machine Learning

This project builds a machine learning pipeline to predict crop yield (kg/ha) based on weather patterns, pesticide usage, and crop/country data. The goal is to better understand which factors influence agricultural productivity and to eventually assist farmers or policymakers with actionable insights.

---

## 📊 Data Sources

- **FAOSTAT (Food and Agriculture Organization)**  
  https://www.fao.org/faostat
- **World Bank Climate Data**  
  https://climateknowledgeportal.worldbank.org/
- **Pesticide Use Dataset**  
  Extracted via FAOSTAT → Inputs → Pesticides

---

## 🧪 Models Used

We trained and compared the following regression models:

- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  
- Support Vector Regressor (SVR)

**Evaluation metrics:**

- R² (Coefficient of Determination)  
- RMSE (Root Mean Squared Error)  
- MAE (Mean Absolute Error)

---

## 📁 Project Structure
```
ml-crop-yield-analysis/
│
├── data/
│ ├── raw/ # Raw input datasets (e.g. climate, pesticides)
│ └── processed/ # Cleaned and merged dataset
│
├── notebooks/ # Jupyter Notebooks for EDA and modeling
├── requirements.txt # Python dependencies
├── README.md # Project overview and setup instructions
└── .venv/ # (optional) Local virtual environment
```

## 📈 Key Results

After testing several models, the **Random Forest Regressor** gave the best results when evaluated crop-by-crop:

| Crop         | R²     | MAE     | RMSE   |
|--------------|--------|---------|--------|
| Barley       | 0.9073 | 363.04  | 541.56 |
| Maize (corn) | 0.8151 | 685.17  | 1069.66|
| Potatoes     | 0.8820 | 2414.69 | 3515.61|
| Rice         | 0.8761 | 464.94  | 740.22 |
| Soya beans   | 0.8080 | 247.71  | 356.41 |
| Wheat        | 0.9302 | 376.93  | 539.53 |

Other models (like Decision Tree and Gradient Boosting) looked promising on overall metrics but performed poorly on individual crops.

---

## 📌 Highlights

- End-to-end ML workflow: data cleaning, feature scaling, modeling, evaluation
- Used One-Hot Encoding for country and crop variables
- Visualized correlations, distributions, and model results
- Plotted feature importances: crop type and pesticides ranked highest
- Explored per-crop prediction accuracy using grouped metrics

---

## 🚀 Future Work

- Train dedicated models for each crop to improve precision
- Add features like soil type, NDVI index, or fertilizer usage
- Apply time-series modeling for yearly prediction trends
- Build a simple web app to recommend yield estimates

---

## 👨‍💻 Author

**Glenn Noronha**  
📍 [GitHub](https://github.com/glennnoronha)

