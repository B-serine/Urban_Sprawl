# Urban_Sprawl
Urban Sprawl Analysis project using multi-decadal Landsat imagery (2000–2024) to classify built-up areas, compute sprawl metrics (growth, compactness, fragmentation), compare multiple cities, and validate results using GHSL with accuracy evaluation and visual dashboards.

# 🌍 Urban Sprawl Analysis Using Multi-Decadal Satellite Imagery (2000–2024)

## 📌 Project Overview
Urban sprawl is one of the major challenges affecting sustainable development, transportation planning, and environmental health.  
This project provides a complete geospatial analytical pipeline to quantify and compare urban sprawl over **20+ years** using **multi-epoch Landsat satellite imagery**.

The system retrieves Landsat data for selected cities across multiple time epochs (e.g., **2000, 2010, 2020, 2024**), classifies land cover into **Built-up vs. Non Built-up**, and computes key sprawl metrics such as growth rate, compactness, fragmentation, and distance-based expansion.

Results are validated using the **Global Human Settlement Layer (GHSL)** and presented through visual dashboards and comparison reports.

---

## 🎯 Objectives
The main objectives of this project are:

- Retrieve Landsat 5/7/8/9 imagery for multiple time epochs (2000–2024)
- Preprocess satellite images (cloud masking, mosaicking, clipping to city boundary)
- Compute spectral indices (e.g., **NDBI**, **BUI**) for built-up detection
- Perform built-up classification using **Random Forest**
- Generate classification maps for each epoch and city
- Compute and analyze urban sprawl indicators:
  - **Total built-up area growth**
  - **Annual growth rate**
  - **Compactness index**
  - **Fragmentation metrics** (patch count, patch size distribution)
  - **Distance from city center analysis**
- Compare results across **3–5 cities**
- Validate classification using **GHSL Built-up Layer**
- Provide visualization dashboards inside Jupyter Notebook

---

## 🛰️ Data Sources
This project uses only open and trusted datasets:

- **Landsat Collection 2 (USGS / Google Earth Engine)**
- **Global Human Settlement Layer (GHSL / GHS-BUILT)**
- **Natural Earth (City boundaries & base layers)**
- **World Urbanization Prospects (UN Population data)** *(optional for correlation analysis)*

---

## 🛠️ Tech Stack
### Core Tools
- **Python (Jupyter Notebook)**
- **Google Earth Engine (GEE)** or **openEO** for satellite data access

### Machine Learning & Spatial Analysis
- **scikit-learn** (Random Forest classification)
- **GeoPandas** (vector processing)
- **Rasterio** (raster processing)
- **PySAL** (spatial analysis)
- **pylandstats** (FRAGSTATS-like landscape fragmentation metrics)

### Visualization
- **Matplotlib**
- **Plotly**
- **Folium / Geemap** *(optional for interactive maps)*

---

---

## 📊 Sprawl Metrics Computed
This project calculates multiple indicators commonly used in urban sprawl research:

### 1. Built-up Area Growth
- Total built-up area (km²) for each epoch
- Absolute growth and percentage increase

### 2. Annual Growth Rate
- Growth rate per year between epochs

### 3. Compactness Index
- Measures how compact or spread the urban footprint is  
  *(compact cities have higher compactness, sprawled cities have lower)*

### 4. Fragmentation Metrics
- Number of urban patches
- Patch size distribution
- Mean patch size

### 5. Distance from City Center Analysis
- Urban density as a function of distance from the center
- Sprawl expansion trend outward from central zones

---

## 🧠 Methodology Summary
1. **Data Retrieval**  
   Landsat imagery is retrieved using Google Earth Engine / openEO.

2. **Preprocessing**
   - Cloud masking
   - Image mosaicking
   - Resampling and clipping to city boundary

3. **Feature Engineering**
   - Compute built-up indices (NDBI, BUI, NDVI)
   - Extract pixel-level features for classification

4. **Classification**
   - Train Random Forest classifier using labeled samples
   - Produce built-up vs. non-built-up maps for each epoch

5. **Sprawl Metrics Computation**
   - Built-up area calculation
   - Landscape metrics (fragmentation, compactness)
   - Distance-based density curve

6. **Validation**
   - Compare classification maps with GHSL built-up dataset
   - Compute accuracy metrics (Precision, Recall, F1-score)

7. **Cross-City Comparison**
   - Compare multiple cities over time
   - Rank cities by growth rate, fragmentation, and compactness

---

## ✅ Validation (GHSL Comparison)
Classification results are validated using the **Global Human Settlement Layer (GHSL Built-up)**.

Validation metrics include:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

---

## 📌 Deliverables
This repository provides:

- ✔ Complete notebook pipeline for multi-epoch urban analysis  
- ✔ Built-up classification maps per epoch per city  
- ✔ Sprawl metrics dashboard (embedded in notebook)  
- ✔ Cross-city comparison analysis  
- ✔ GHSL validation and accuracy metrics  

---

## 🚀 How to Run the Project

### 1️⃣ Clone Repository

git clone https://github.com/your-username/urban-sprawl-analysis.git
cd urban-sprawl-analysis

### 2️⃣ Install Dependencies
pip install -r requirements.txt

### 3️⃣ Run Jupyter Notebook
jupyter notebook

Then open the notebooks in the notebooks/ folder in order.
