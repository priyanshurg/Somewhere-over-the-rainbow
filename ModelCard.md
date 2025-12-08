# Cowerful Model Card
### Predicting Dairy Farm Carbon Footprint Using the Arla Foods Decarbonization Dataset

## Overview
Cowerful is an interactive ML tool that predicts the carbon footprint of a dairy farm in **kg CO₂e per kg FPCM** (fat-and-protein-corrected milk). The tool is built on real operational data from **Arla Foods**, one of the world’s largest dairy cooperatives.

Farmers can adjust sliders representing their farm’s practices, inputs, and biological performance. The model then:
1. Predicts carbon footprint
2. Interprets feature impacts using SHAP
3. Compares the farmer's inputs to real farms in the dataset
4. Suggests realistic mitigation strategies

---

## Data Source
The model is trained on the **Arla Foods Data-Driven Decarbonization Dataset**, consisting of **10,000 farm-year observations** across Europe.

Each farm measures:
- Feed use
- Nitrogen flows
- Land use
- Manure management
- Energy sourcing
- Grazing intensity
- Soy inclusion
- Mortality rates
- Permanent grassland area

---

## Model Objective
**Output variable:**  
- `Carbon_footprint`: kg CO₂e per kg FPCM  
This includes methane, nitrous oxide, and CO₂ emissions.

**Key GHG categories:**
- Enteric methane  
- Manure methane  
- Nitrous oxide (fertilizer and manure)  
- Upstream feed production  
- Energy emissions  

---

## Model Architecture
- **Algorithm:** Gradient-boosted decision trees (XGBoost or LightGBM)
- **Task:** Regression
- **Training:** 80/20 split with cross-validation
- **Explainability:** SHAP additive explanations

This structure was chosen because:
- Tree models handle non-linear interactions
- SHAP gives transparent, farmer-friendly explanations
- Model performs well on mixed continuous/binary data

---

## Prediction Workflow
1. Farmer adjusts sliders  
2. Model receives structured feature vector  
3. Prediction is generated  
4. SHAP values explain impact of each feature  
5. Cowerful compares farmer values to dataset percentiles  
6. Advice module provides actionable recommendations

---

## Limitations
- Extreme outliers may not be well-explained (values outside dataset range)
- Economic trade-offs are not modeled
- Weather, soil type, and breed genetics are not included
- SHAP provides correlations, not causation

---

## Intended Use
Cowerful is designed to:
- Help farmers understand their emissions drivers  
- Highlight improvement opportunities  
- Compare farm performance to peer benchmarks  
- Support data-driven climate action  
