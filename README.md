# 🌍 Land Use Change in Indonesia: Monitoring Zero-Deforestation Commitment Using Remote Sensing

This project addresses the question: **"To what extent is the zero-deforestation commitment being upheld in Indonesia?"** The study focuses on classifying land use changes from vegetation (rainforest, shrubland, wetland) to palm oil plantations between two time points. A representative project area was selected in the southern part of Borneo (Indonesia), specifically in the provinces of Kalimantan Selatan and Kalimantan Tengah. The study was conducted as part of the module **"Applied Remote Sensing in Geoscience"** at TU Bergakademie Freiberg during the winter semester 2024-25.  
This repository contains the implementation of land use classification and change detection in the form of a Jupyter Notebook. The analysis is based on Sentinel-2 data and uses machine learning to identify land use changes between two time points.

---

## 📋 **Overview**

- **Project Area:** Selected based on research on forest area changes in Indonesia (Borneo, Kalimantan Selatan and Tengah).
- **Data Source:** Sentinel-2 raster data (bands B02-B12) with <10% cloud cover, captured in the same season.
- **Software & Libraries:** Python 3.8.18, Jupyter Notebook, and libraries such as `rasterio`, `geopandas`, `numpy`, `scikit-learn`, `matplotlib`, `tqdm`.
- **Training Data:** Polygons of land use classes (e.g., rainforest, palm oil) created in QGIS and saved as Shapefiles.
- **Data Preparation:** Resampling 20 m resolution bands to 10 m, extracting pixel values, and converting them to reflectance values.
- **Model Training:** Random Forest with 200 decision trees, using 70% of the data for training and 30% for testing.
- **Classification:** Applying the model to raster data, outputting GeoTIFFs (classification and confidence maps).
- **Smoothing:** Removing small pixel groups (<200 pixels) using the `sieve` function.
- **Change Detection:** Comparing classification results from 2019 and 2023, focusing on rainforest, shrubland, wetland, and palm oil plantations.
- **Results:** Changes in land cover analyzed and visualized in tables, diagrams, and GeoTIFFs.

---

## 📂 **Access to Data**
The Sentinel-2 raster data is not included in this repository but can be downloaded from the following Google Drive link:

[📂 **Google Drive Folder**](https://drive.google.com/drive/folders/1B8sOcUJ7OA7zvgymPTMpvX0zoLoPXuAO?usp=sharing)

### **Files in the Google Drive Folder**
- **Input Data:** Sentinel-2 raster data (`*.jp2`)

Place the files in the appropriate directory:
- **Input Data:** `input_dir`

---

## 🚀 **Usage**
The script was tested in **Google Colab Pro** with extended RAM due to the high memory requirements for processing Sentinel-2 data.

### **Steps to Execute**
1. **Clone the repository:**
   ```bash
   git clone https://github.com/ErikFranke/Sentinel2-LandUseChange-Indonesia.git
   cd Sentinel2-LandUseChange-Indonesia
   
2. **Download the Sentinel-2 data:**
   Download the data from the [Google Drive Folder](https://drive.google.com/drive/folders/1B8sOcUJ7OA7zvgymPTMpvX0zoLoPXuAO?usp=sharing) and place it in the `input_dir` directory.

3. **Open the script in Google Colab:**
   Upload the file `remote_sensing_class-change_indo-forest_colabCPU.ipynb` to Google Colab.

4. **Run the script:**
   ⚙️ **Requirements:** Ensure the following Python libraries are installed:
   - `rasterio`
   - `geopandas`
   - `tqdm`
   - `matplotlib`
   - `scikit-learn`
   - `joblib`

   Follow the instructions in the script (e.g., adjusting file paths, etc.).

---

## 📜 **License**
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

Good luck with your analysis! 🚀
