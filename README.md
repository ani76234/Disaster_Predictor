# 🌍 ML-Based Disaster Prediction System

A machine learning project for studying environmental patterns across India and predicting disaster categories using geographically extracted environmental data.

The project combines **Google Earth Engine-based data extraction, environmental feature analysis, and Random Forest classification** to identify patterns associated with four disaster categories:

- 🌊 Flood
- ⛰️ Landslide
- ☀️ Drought
- 🌀 Cyclone

---

## 📌 Project Overview

The objective of this project was to investigate whether environmental and geographical conditions could be used to identify patterns associated with different types of natural disasters across India.

Rather than relying on a pre-existing machine learning dataset, the dataset was **compiled from environmental and geospatial information extracted using Google Earth Engine**.

The resulting dataset was then analyzed and used to train a Random Forest classification model.

### Project Pipeline

```text
Google Earth Engine
        ↓
Environmental & Geospatial Data Extraction
        ↓
Custom "Extracted Dataset"
        ↓
Data Preparation & Analysis
        ↓
Random Forest Classification
        ↓
Disaster Prediction + Class Probabilities
```

---

## 🛰️ Data Collection

Environmental and geographical data were extracted using **Google Earth Engine** and compiled into a custom dataset for studying general environmental patterns across India.

The extracted variables include:

- Elevation
- Temperature
- Rainfall
- Soil Moisture
- Vegetation Index
- Slope
- Distance to River
- Distance to Coast
- Wind Speed
- Soil Type

The resulting dataset is stored as:

```text
Extracted Dataset.csv
```

The dataset was created specifically for this project by compiling environmental observations from Google Earth Engine rather than using a ready-made machine learning dataset.

---

## 🌱 Features

| Feature | Description |
|---|---|
| Elevation | Elevation of the location |
| Temperature | Environmental temperature |
| Rainfall | Rainfall measurements |
| Soil Moisture | Soil moisture conditions |
| Vegetation Index | Vegetation-related environmental indicator |
| Slope | Terrain slope |
| Distance to River | Distance from the nearest river |
| Distance to Coast | Distance from the coastline |
| Wind Speed | Wind conditions |
| Soil Type | Soil classification |

These environmental and geographical variables were used to study patterns associated with different disaster categories.

---

## 🧠 Machine Learning Approach

### Random Forest Classification

A **Random Forest Classifier** was used to classify environmental conditions into four disaster categories:

```text
Flood
Landslide
Drought
Cyclone
```

Random Forest was selected as the primary model because it can capture nonlinear relationships between multiple environmental variables through an ensemble of decision trees.

### Model Configuration

```python
RandomForestClassifier(
    n_estimators=300,
    max_depth=15,
    random_state=42
)
```

### Dataset Split

- **70%** training data
- **30%** testing data
- Random state: `42`

---

## 📊 Model Performance

The trained Random Forest model achieved:

| Metric | Score |
|---|---:|
| **Accuracy** | **88.27%** |
| **Macro F1-Score** | **0.81** |

The model was evaluated on a held-out test set.

In addition to overall accuracy, precision, recall, and F1-score were evaluated across individual disaster classes to assess classification performance.

---

## 🔮 Prediction System

The trained model produces:

1. **Predicted disaster category**
2. **Probability for each disaster category**

For example:

```text
Predicted Disaster: Landslide

Flood:      2.1%
Landslide: 95.7%
Drought:    1.4%
Cyclone:    0.8%
```

The probability output provides a more informative representation of the model's prediction than a single classification label.

---

## 🛠️ Technologies Used

- **Python**
- **Google Earth Engine**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Jupyter Notebook**
- **Random Forest**
- **Classification Metrics**

---

## 📁 Project Structure

```text
Disaster-Prediction/
│
├── Random_Forests_Disaster_Prediction.ipynb
├── Extracted Dataset.csv
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/disaster-prediction.git
cd disaster-prediction
```

### 2. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Random_Forests_Disaster_Prediction.ipynb
```

Make sure `Extracted Dataset.csv` is located in the same directory as the notebook.

---

## 🔬 Key Contributions

- Compiled a custom environmental dataset using **Google Earth Engine**
- Studied general environmental patterns across **India**
- Integrated multiple geographical and environmental variables into a machine learning workflow
- Developed a **4-class disaster classification system**
- Trained a **300-tree Random Forest ensemble**
- Achieved **88.27% test accuracy**
- Achieved **0.81 macro F1-score**
- Implemented probability-based disaster risk predictions

---

## 📈 Future Improvements

Potential extensions include:

- Hyperparameter optimization using Grid Search or Randomized Search
- Cross-validation for more robust evaluation
- Feature importance and model explainability
- Integration of additional satellite-derived variables
- Geographic visualization of predicted disaster risks
- Integration with real-time environmental data
- Comparison with XGBoost, LightGBM, and other ensemble models
- Development of a web-based disaster risk prediction dashboard

---

## 👨‍💻 Author

**Anirudh Sharma**  
B.Tech Mathematics & Computing  
Manipal Institute of Technology
