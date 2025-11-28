# 🗺️ GeoTarget Webapp: Interactive Locality Visualization & Targeting Tool

This project is a **Streamlit-based geospatial webapp** for visualizing and exploring administrative boundaries (ADM2 and ADM3). It allows users to filter departments, highlight communes, and interact with an automated **Folium** map.

This tool is highly effective for **targeting**, **field planning**, and **geospatial insight generation** across development, program management, and business operations.

---

## 🚀 Key Features

* **Interactive Geographic Map:** Built using the Folium library for high-quality, zoomable map interactions.
* **Intuitive Selection:** Sidebar controls for selecting and filtering administrative divisions at the **department (ADM2)** and **commune (ADM3)** levels.
* **Color-Coded Layers:** Orange for selected communes, Light green for other communes.
* **Boundary Visualization:** Clear department-level boundary outlines.
* **Automated Labeling:** Automatic centroid labeling for administrative areas.
* **Performance:** Geometry simplification for fast rendering and cached shapefile loading for efficient use.
* **Customizable:** Fully adaptable for any country's administrative shapefile.

---

## 💡 Potential Use Cases

* Identifying priority **target areas** for resource allocation.
* Planning **field survey routes** or monitoring visits.
* Visualizing **coverage gaps** in service delivery.
* Supporting **operational and program decisions**.
* Mapping **clusters**, **zones**, and **local administrative divisions**.
* Creating sharable **interactive spatial dashboards**.

---

## 🧰 Tech Stack

### Core Libraries

* **Python**
* **Streamlit** (for web deployment)
* **GeoPandas** (for geospatial data handling)
* **Folium** (for interactive mapping)
* **Shapely** (for geometric operations)
* **streamlit-folium** (for integrating the map)

---

## ▶️ How to Run the App

### 1. Setup

First, clone the repository using `git clone <your-repo-url>`, then navigate into the directory using `cd <repository-name>`. Next, install all Python dependencies using `pip install -r requirements.txt`.

### 2. Execution

Run the Streamlit application with the command `streamlit run app.py`. Your browser will open automatically with the interactive map interface.

---

## 📂 Data Requirements

To function properly, your shapefile must include:

* An ADM2 column (e.g., `name_2`)
* An ADM3 column (e.g., `name_3`)
* Valid polygon geometries

> **Example dataset used in this project:**
> Stanford Geoportal – Chad Administrative Boundaries
> `https://geo.nyu.edu/catalog/stanford-tq540mj3859`

Ensure all necessary shapefile components (`.shp`, `.shx`, `.dbf`, etc.) are present in the `datafiles/` directory.

---

## ⚙️ Customization Options

The main application function (`launch_commune_map_app()`) allows configuration of key parameters to adapt the tool to any project context:

* `shapefile_path` – Path to your ADM3 shapefile
* `adm2_col` – Department column name
* `adm3_col` – Commune column name
* `default_depts` – Default selected ADM2 departments
* `map_center` – Initial map center coordinates
* `map_zoom` – Starting zoom level

---

## 📝 Notes

* Geometry simplification improves performance for large shapefiles.
* Shapefile caching significantly speeds up reload time.
* Centroid projections can be updated depending on the geographic region.
* Folium allows lightweight map rendering directly in the browser.

---

## 📬 Contact

**Hashir Bawany**
* 📧 Email: `your email here`
* 🔗 LinkedIn: `your LinkedIn here`
