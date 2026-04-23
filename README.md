# Kaggle Competition – Sofia ML Regression 2026 Winter

## 🏆 Result
Ranked **#1 on the final (private) leaderboard** in a regression-focused machine learning competition.

![Leaderboard](images/kaggle-rank.png)
*Final private leaderboard showing 1st place ranking*

Competition:
https://www.kaggle.com/competitions/sofia-ml-regression-2026-winter

---

## 📊 Overview

The key insight behind this solution was identifying that the dataset exhibited **two distinct regimes**:

- ~93% of the data followed a **linear relationship**
- ~7% of the data followed a **quadratic relationship**

Instead of applying a single model, I designed a hybrid approach to handle both patterns effectively.

---

## ⚙️ Approach

### 1. Data Preprocessing
- Filled missing values using **median imputation**
- Identified outliers using **IQR (Interquartile Range)**

---

### 2. Data Segmentation
- Split dataset into:
  - **Normal rows (~93%)**
  - **Extreme rows (~7%)**

---

### 3. Model for Normal Data
- Trained **Linear Regression** on normal rows only  
- Added squared features  
- Applied scaling for stability  

---

### 4. Extreme Data Insight
Through analysis, discovered:

target ≈ 5 × x1²  

This relationship was derived from data inspection, not learned by the model.

---

### 5. Final Model (Blending)

ŷ = 0.9 × Linear Model + 0.1 × (5 × x1²)

- Linear model captures general trends  
- Formula handles extreme cases  
- Blending improves overall performance  

---

## 📈 Results

- **Private Leaderboard:** #1  
- **Public Leaderboard:** Low (no extreme rows present)  
- **Cross-Validation:** ~0.0819 (consistent with private score)  

---

## 🧠 Key Learnings

- EDA is critical for uncovering hidden patterns  
- Outliers can represent meaningful structure  
- Simple models + insight outperform complex models  
- Cross-validation prevents overfitting  
- Hybrid approaches improve robustness  

---

## 📁 Repository Contents

- `Competition Submitted Notebook.ipynb` → full solution notebook  
- `images/kaggle-rank.png` → leaderboard proof  

---

## ⚠️ Notes

- Dataset not included due to competition rules  
- Code is structured for reproducibility  

---

## 🔗 Links

- Competition:  
  https://www.kaggle.com/competitions/sofia-ml-regression-2026-winter  

- Kaggle Profile:  
  https://www.kaggle.com/phoenix01revv  
