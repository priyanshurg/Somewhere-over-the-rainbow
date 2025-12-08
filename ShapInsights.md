# SHAP Insights for Cowerful

SHAP values explain how each feature moves a farm's carbon footprint prediction up or down relative to the average.

---

## Features that Typically INCREASE Emissions
### 1. High Feed_inefficiency
- Needing more feed per kg milk increases both methane and upstream feed emissions.

### 2. High Fertilizer_use
- Strong driver of nitrous oxide (N₂O), a potent greenhouse gas.

### 3. High Soy_use
- Linked to deforestation and land use change emissions.

### 4. High Animal_mortality
- More replacement animals required → more emissions.

### 5. Low Renewable_electricity_use
- Increases carbon intensity of milking and cooling operations.

---

## Features that Typically DECREASE Emissions
### 1. High Protein_efficiency
- More nitrogen converted into milk and meat → less N lost as N₂O.

### 2. Manure_mgmt = 1 (biogas/acidification)
- Slurry acidification or biogas conversion greatly reduces methane.

### 3. Higher Grazing
- Reduces feed production emissions, improves soil carbon sequestration.

### 4. Higher Permanent_grassland
- Farms with well-managed permanent grassland often rely less on imported feed.

---

## SHAP Rules of Thumb
- **Positive SHAP** → increases carbon footprint  
- **Negative SHAP** → decreases carbon footprint  
- **Magnitude** = strength of effect  
