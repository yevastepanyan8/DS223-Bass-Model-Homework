# Innovation Diffusion Analysis — Bass Model
**Course:** DS-223  
**Student:** Karen Hovhannisyan  
**Date:** September 24, 2025  
**Points:** 50  
**Deadline:** 2025-10-03  

---

## 📖 Project Overview
This project applies the **Bass Diffusion Model** to analyze and forecast the adoption of Samsung’s **Neo QLED 8K TV** innovation (from TIME’s 2024 Innovations List).  
To estimate Bass parameters, historical adoption data of **LCD TVs** was used as a look-alike innovation.

The goal is to:
1. Estimate parameters (p, q, M) using historical data.  
2. Predict the diffusion path of the Neo QLED 8K TV.  
3. Estimate the number of adopters per period.  
4. Interpret results and visualize adoption curves.

---

## 🧩 Data Sources
- **OLED / LCD TV shipments (2016–2023)** – from Statista and industry reports (used for global analysis).  
- **Sony LCD TV unit sales (2012–2022)** – used for manufacturer-level comparison.  
- All data are stored in the `/data/` directory in `.csv` format.

---

## 🧮 Methods
- Implemented the **Bass Diffusion Model** using `R` and `nls()` (non-linear least squares).  
- Parameters estimated:
  - **p**: coefficient of innovation (external influence)  
  - **q**: coefficient of imitation (social influence)  
  - **M**: market potential (total expected adopters)
- Visualizations made with `ggplot2`.

---

## 📊 Results Summary
| Parameter | Description | Estimated Value |
|------------|--------------|----------------:|
| p | Innovation coefficient | 0.00824 |
| q | Imitation coefficient | 0.6304 |
| M | Market potential (millions) | 40.61 |

- Peak adoption around **late 2022**.  
- Total expected adopters ≈ **40.3 million units** (lifetime).  
- The Neo QLED 8K TV likely follows similar dynamics, with stronger imitation effects due to social and visual influence.

---

## 🌍 Scope
- Analysis performed on **global shipments** (2016–2023).  
- Supplementary manufacturer-level data from Sony used for comparison.  
- Predictions extended to **2030**.

---

## 🗂️ Project Structure
project_root/
│
├── README.md 
│
├── data/ 
│ ├── dataset1.xlsx
│ └── predicted_adopters_2016_2030.csv
│
├── img/
│ └── observed_vs_pred.png
│
├── report/ 
│ ├── report.pdf
│ └── report_source.Rmd
│
└── project_description.pdf
