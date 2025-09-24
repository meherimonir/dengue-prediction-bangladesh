# Dengue Prediction Dataset (Bangladesh, 2021–2025)

This repository contains the dataset used in our study **"Dengue Prediction Using Google Search Trends: A Machine Learning Approach"**.  
The dataset combines Google Search Trends and official dengue case reports to support predictive modeling of dengue outbreaks in Bangladesh.

Files in This Repository

1. `dengue_rev.csv` (Raw Dataset)
- Collected directly from Google Search Trends (weekly data, Dec 2021 – Jun 2025).  
- Keywords include dengue-related terms in both English and Bangla (e.g., "Dengue", "Dengue জ্বর", "CBC Test", "Platelet count").  
- Daily dengue case counts were obtained from Directorate General of Health Services (DGHS) and aggregated to weekly totals.  
- This file represents the raw, unprocessed data as collected.

2. `dengue_res.csv` (Processed Dataset – Min–Max Scaled)
- Preprocessed from `dengue_rev.csv` using the following pipeline:
  1. **Anchor Method:** “Dengue” term used as reference to align other keywords.  
  2. **Value Correction:** Replaced all `<1` values with `1` to avoid loss of information.  
  3. **Normalization:** Applied Min–Max scaling (0–100) to standardize features.  
  4. **Missing Values:** Filled with `1` (rare blanks from Google Trends).  
- This is the exact dataset used for training and evaluation in the paper.
