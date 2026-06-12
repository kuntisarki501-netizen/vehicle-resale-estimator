# Intelligent Used Vehicle Resale Estimator

**Techaxis Data Science Internship 2026 — Week 1 Proposal**
---
## Intern Details

| Field | Details |
|-------|---------|
| **Intern** | Kunti Sarki |
| **Date** | 11 June, 2026 |

---
## Business Problem

Vehicle dealers and individual sellers in Nepal struggle to determine fair
resale prices for used cars. Manual pricing is slow, inconsistent, and often
unfair to both buyers and sellers. This tool automates resale price prediction
and explains exactly why a vehicle is priced at that value using Explainable AI.

---

## What I'm Building

A Streamlit web app that:

- Takes vehicle details as input (brand, year, km driven, fuel type, transmission, owner history)
- Predicts the resale price using an XGBoost regression model
- Displays a **Gauge Chart** showing Low → Fair → High price range
- Uses **SHAP Waterfall Plot** to explain why the price is what it is *(e.g. "High mileage reduced value by Rs. 1,20,000")*
- Uses an **LLM** to generate a 2-sentence Investment Summary based on predicted price and vehicle features
- Includes a **RAG Chatbot** *(Week 6)* to answer Nepal vehicle market questions *(e.g. "Which brand holds value best?")*

---

## Dataset

- **Primary Dataset:** Car Details v3 — CarDekho Dataset (7,000+ used car listings, 13 features)
  https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho

- **Synthetic Features Added:**
  - `condition` — engineered from owner history (First Owner → Excellent)
  - `car_age` — engineered from year column
  - `brand` — extracted from name column
  - `selling_price_npr` — INR × 1.6 Nepal price adjustment

---

## Success Metrics

| Metric | Target |
|--------|--------|
| Model R² Score | ≥ 0.85 |
| RMSE | < Rs. 1,50,000 |
| SHAP Explanation | Top 5 features explained |
| Deployment | Live Streamlit app by Week 7 |

---

## Weekly Plan

| Week | Topic | Key Deliverable |
|------|-------|----------------|
| **Week 1** | Dataset sourcing, data inspection, GitHub repo init | Proposal + Repo URL |
| **Week 2** | Data cleaning, EDA, correlation heatmap | EDA Notebook + PDF |
| **Week 3** | Feature engineering (car_age, brand, condition), baseline model | Feature Notebook |
| **Week 4** | XGBoost tuning with Optuna, SHAP waterfall, save model.pkl | Optimized Model |
| **Week 5** | LLM integration (Investment Summary generation) | LLM Notebook |
| **Week 6** | RAG chatbot over Nepal vehicle market knowledge base | Chatbot Demo |
| **Week 7** | Streamlit app + Gauge Chart + deploy to Streamlit Cloud | Live URL |
| **Week 8** | Business report, portfolio case study, final video | Final Submission |

---

## Tech Stack

Python, Pandas, Scikit-Learn, XGBoost, Optuna, SHAP,
LangChain, OpenAI API / Gemini, FAISS, Streamlit, Git

## Submission Links 
**Dataset** - https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho
**GitHub Repo** - https://github.com/kuntisarki501-netizen/vehicle-resale-estimator.git
---

