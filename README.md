

# 🛡️ Intelligent Pipeline Integrity & Corrosion Growth Engine

> **Automated ILI Alignment, Corrosion Growth Analysis, and Interaction Zone Detection**

---

## 📌 Problem Statement

Inline Inspection (ILI) runs from different years cannot be directly compared due to **odometer drift**, **vendor inconsistencies**, and **feature renaming**.
As a result, corrosion growth tracking is unreliable, manual, and error-prone — directly impacting pipeline safety decisions.

---

## 🎯 Objective

Build an **end-to-end analytics pipeline** that:

* Aligns multiple ILI runs onto a **common physical reference**
* Accurately **matches corrosion anomalies across time**
* Computes **growth rates** with engineering integrity
* Identifies **high-risk interaction zones**
* Presents results through an **interactive dashboard**

---

## 🧠 Solution Overview

We designed a **physics-aware, industry-aligned workflow** used by commercial integrity platforms.

### High-Level Architecture

```
ILI Data (2015, 2022)
        ↓
Data Standardization
        ↓
Anchor-Based Alignment (Common Ruler)
        ↓
Multi-Factor Anomaly Matching
        ↓
Growth & Risk Computation
        ↓
DBSCAN Interaction Zones
        ↓
Streamlit Dashboard
```

---

## ⚙️ Key Technical Innovations

### 1. Rubber-Sheeting Alignment (Common Ruler)

* Uses **fixed pipeline features** (Valves, Tees, Taps, Bends)
* Matches anchors via **Elevation fingerprinting**
* Applies **piecewise linear interpolation**
* Corrects non-linear odometer drift across 57,000+ ft

> Result: 2022 data mapped precisely onto the 2015 physical pipeline

---

### 2. Industry-Grade Anomaly Matching

Each corrosion feature is matched using:

* **Corrected distance** (±10 ft)
* **Clock position geometry** (circular angle math)
* **ID/OD consistency**
* **Dimensional similarity (length & width)**

Outputs:

* Verified Matches (High Confidence)
* Uncertain Matches (Flagged for review)
* New Anomalies (Unknown growth)
* Missing Anomalies (Repaired or inactive)

---

### 3. Scientifically Honest Growth Calculation

* Uses exact inspection interval: **6.8 years**
* Computes:

  * Depth growth (%)
  * Length growth (in)
  * Width growth (in)
  * Annualized rates
* **No assumptions** for new anomalies (kept as NaN)

---

### 4. Interaction Zone Detection (DBSCAN)

* Clusters nearby corrosion features
* Identifies **252 Interaction Zones**
* Highlights areas where defects **interact structurally**
* Prioritizes dig planning over isolated pit analysis

---

## 📊 Key Results

| Metric                  | Result           |
| ----------------------- | ---------------- |
| Verified Matches        | **532**          |
| Max Depth Growth        | **49%**          |
| Avg Growth Rate         | **~0.6% / year** |
| Interaction Zones       | **252**          |
| Pipeline Length Aligned | **~57,300 ft**   |

📈 Growth distribution follows a **shifted Gaussian**, validating matching accuracy while isolating a high-risk tail.

---

## 🖥️ Visualization Dashboard (Streamlit)

Features:

* KPI overview (Active threats, Max growth, Zones)
* Unity plot with tolerance band
* Pipeline risk profile
* Corrosion bloom histogram
* Cluster-level risk tables

Launch:

```bash
streamlit run app.py
```

---

## 📂 Repository Structure

```
├── data/
│   ├── ILIDataV2.xlsx
│
├── notebooks/
│   ├── Phase1_Alignment.ipynb
│   ├── Phase2_Matching.ipynb
│   ├── Phase3_Clustering.ipynb
│
├── app.py                     # Streamlit dashboard
├── Final_Submission_Expert.csv
├── Final_Submission_With_Clusters.csv
├── README.md
```

---

## 🧪 Technologies Used

* **Python**
* pandas, numpy
* scikit-learn (DBSCAN)
* matplotlib, seaborn, plotly
* Streamlit

---

## 🚀 Future Enhancements (Industry Roadmap)

* Dynamic Time Warping for non-linear slips
* Probabilistic confidence modeling
* GIS integration (lat/long mapping)
* Remaining life (RUL) prediction
* Automated dig-sheet generation
* Real-time ILI ingestion pipeline

---

## 🏆 Why This Matters

This project moves beyond academic matching and delivers:

* **Safety-driven decision support**
* **Engineering honesty**
* **Actionable outputs for integrity teams**

It mirrors how **commercial integrity platforms** operate — with transparency, uncertainty handling, and risk prioritization.

---

## 👤 Author

**Raj Purohith Arjun**

**Venkateswarlu N**
MS Data Science — Texas A&M University


---


