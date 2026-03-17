# AI-Based Forest Fire Prediction & Spread Simulation using ML and Cellular Automata

An end-to-end geospatial machine learning and simulation system to predict forest fire risk and model wildfire spread.

 **Case Study:** Uttarakhand, India

---

## Overview

Forest fires pose a significant threat to ecosystems, biodiversity, and human settlements. This project combines **Machine Learning** and **Cellular Automata (CA)** to:

- Predict fire-prone regions using environmental and geospatial data  
- Simulate wildfire spread dynamically over time  

The system integrates satellite-derived features such as vegetation, temperature, and terrain to model real-world fire behavior.

---

## Objectives

- Predict forest fire risk using ML models  
- Simulate wildfire spread using Cellular Automata  
- Evaluate model performance using ROC-AUC, Precision-Recall, and Confusion Matrix  
- Provide insights for proactive wildfire management  

---

## Tech Stack

- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost  
- **Geospatial Tools:** Raster processing, satellite data (NDVI, LST)  
- **Environment:** Jupyter Notebook  

---

## Methodology

### Data Processing
- Integrated geospatial datasets:
  - NDVI (vegetation index)
  - LST (land surface temperature)
  - Precipitation
  - Elevation, slope, aspect
  - Distance to roads (human factor)

---

### Machine Learning Models

- **XGBoost**
- **Random Forest (Best Performing Model)**

Handled class imbalance using:
- `scale_pos_weight` (XGBoost)
- `class_weight="balanced"` (Random Forest)

---

### Model Evaluation

- Accuracy  
- ROC-AUC  
- Precision-Recall Curve  
- Confusion Matrix  

---

## Model Performance

| Model          | Accuracy | ROC-AUC | Precision (Fire) | Recall (Fire) | F1 Score |
|----------------|---------|--------|-----------------|--------------|----------|
| XGBoost        | 73.29%  | 0.784  | 0.79            | 0.76         | 0.78     |
| Random Forest  | 78.22%  | **0.815** | 0.79        | **0.88**     | 0.83     |

---

## Visualizations

### Confusion Matrix
![Confusion Matrix]<img width="444" height="393" alt="image" src="https://github.com/user-attachments/assets/15a5856a-7f81-4f27-aaa2-66b70b2907ba" />


### ROC Curve
![ROC Curve]<img width="536" height="470" alt="image" src="https://github.com/user-attachments/assets/fb00902c-0af7-46f0-b35e-beecb8f31381" />


### Precision-Recall Curve
![PR Curve] <img width="545" height="470" alt="image" src="https://github.com/user-attachments/assets/07e5d92b-30e5-438c-8685-5e77acfc674b" />


### Feature Importance
![Feature Importance]<img width="793" height="451" alt="image" src="https://github.com/user-attachments/assets/a584330f-6d23-47b0-9ecd-ea933e1ecccf" />


---

## Key Insights

- Random Forest outperformed XGBoost across all metrics  
- High recall (0.88) ensures minimal missed fire events  
- Elevation, NDVI, and temperature are the most influential features  
- Human activity (distance to roads) also impacts fire occurrence  

---

## Simulation (Cellular Automata)

- Grid-based wildfire simulation  
- Fire spreads based on:
  - Neighboring cells  
  - Environmental conditions  
- Models dynamic fire propagation over time  

---

## Simulation Metrics

- % Area burned  
- Fire spread rate  
- Time-step based propagation  

---

## Project Structure
forest-fire-prediction-cellular-automata/
│
├── notebook.ipynb
├── data/
├── images/
├── README.md
└── requirements.txt


---

## 🚀 How to Run

```bash
git clone https://github.com/your-username/forest-fire-prediction-cellular-automata.git
cd forest-fire-prediction-cellular-automata
pip install -r requirements.txt
```
google colab notebook

Author
Ankit Kumar
connect.ankitkumar@gmail.com
