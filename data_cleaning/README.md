# 📁 Data Cleaning Overview

This folder contains notebooks that perform the **data quality cleaning** stage of the TFT analytics pipeline.  
For raw data curation and source details, refer to the project root `README.md`.

---

## 📘 Notebooks

### **1. 01_data_integration.ipynb**
- Downloads and extracts *Data Dragon* JSON (version 15.7.1)
- Builds champion and item reference tables
- Explodes `tft_matches_flat.csv` into a long-format unit-level dataset
- **Outputs**:  
  - `tft_units_long.csv.gz`  
  - `champ_ref.csv.gz`

### **2. 02_cleaning.ipynb**
- Profiles missing values, duplicates, and memory usage  
- Applies rule-based and automatic regex normalization for champion names  
- Drops residual non-champion tokens (e.g. *Beardy*, *JayceSummon*)  
- Freezes environment versions for reproducibility  
- **Outputs**:  
  - `tft_units_long_clean.csv.gz`  
  - `tft_units_long_clean.meta.json`  
  - `requirements.txt` (saved to project root)

---

## ✅ Data Quality Summary

- **Duplicates**: All row-level and key-level duplicates removed  
- **Unmatched champions**: Units not tied to official LoL champions dropped (~12.8%)  
- **Outliers**: Column `gold_left_outlier` added via IQR filtering  

---

## 🧾 Provenance & Reproducibility

- Each cleaned file is paired with a `.meta.json` logging generation time and row count  
- Package versions locked in `requirements.txt`  
- Outputs are deterministic across machines with identical inputs and environment  
