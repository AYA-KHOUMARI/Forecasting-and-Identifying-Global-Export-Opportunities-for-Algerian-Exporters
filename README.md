# 🇩🇿 Forecasting and Identifying Global Export Opportunities for Algerian Exporters

> An end-to-end machine learning system that identifies, analyzes, and forecasts international export opportunities for Algerian exporters across agriculture, industry, and services sectors.

---

##  Project Overview

Algeria's export economy is heavily concentrated in hydrocarbons (~92% of total exports in 2023). This project addresses the strategic need for export diversification by building a data-driven ML system that:

- Analyzes global trade flows by product, country, and sector
- Identifies untapped international markets for Algerian exporters
- Discovers high-demand products Algeria could potentially export
- Forecasts future trade volume and value trends

The system supports institutions such as **CACI** (Algerian Chamber of Commerce and Industry) and the **Ministry of External Commerce** in strategic planning.

---

##  Objectives

- Collect and integrate trade data from multiple sources (UN Comtrade, WTO, Trade Map, World Bank)
- Engineer meaningful economic features (growth rates, market share, demand indicators)
- Apply **clustering** to group countries, products, and sectors by trade patterns
- Build **classification** models to detect high-opportunity export markets
- Develop **forecasting** models to predict trade trends by product and country
- Deploy an interactive **visualization dashboard** for exporters and policymakers

---

##  Project Structure

```
algerian-export-opportunities/
├── data/
│   ├── raw/                        # Raw data from UN Comtrade, WTO, etc.
│   ├── processed/                  # Cleaned, merged, and encoded data
│   └── README.md                   # Dataset sources and description
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_preparation_eda.ipynb
│   ├── 03_clustering.ipynb
│   ├── 04_classification.ipynb
│   └── 05_forecasting.ipynb
├── src/
│   ├── data_loader.py              # Multi-source data ingestion
│   ├── feature_engineering.py      # Growth rates, demand index, etc.
│   ├── clustering.py               # Country/product clustering
│   ├── classification.py           # Export opportunity detection
│   ├── forecasting.py              # Trade trend prediction
│   └── evaluation.py              # Metrics and model evaluation
├── dashboard/
│   ├── grafana/                    # Grafana dashboard config
│   └── pipeline.py                 # Data pipeline (API/DB/CSV ingestion)
├── results/
│   └── figures/                    # Visualizations and plots
├── report/                         # Final technical report
├── requirements.txt
└── README.md
```

---

##  Data Sources

### Data Sources
| Source | Description | Link |
|--------|-------------|------|
| CEPII BACI HS92 | Bilateral trade flows 1995–2024, 200+ countries, 5000+ products | [Download](https://www.cepii.fr/CEPII/en/bdd_modele/bdd_modele_item.asp?id=37) |
| CEPII GeoDist | Geographic & colonial features for country pairs | [Download](https://www.cepii.fr/CEPII/en/bdd_modele/bdd_modele_item.asp?id=6) |
| World Bank API | Macroeconomic indicators 1995–2024 | Pulled via `wbgapi` in notebook |

All datasets are publicly available and comply with data privacy requirements.

    
---

##  Methodology

### Step 1 : Data Collection

- International trade data (exports/imports by product and country)
- Economic indicators (GDP, trade growth, market size)
- Algerian export data from public sources
- Sectoral and product-level trade statistics
  
### Step 2 : Data Preparation & Feature Engineering

- Cleaning and harmonizing multi-source datasets
- Handling missing values and inconsistencies
- Engineered features:
  - Export growth rate
  - Global demand index
  - Market penetration ratio
  - Trade balance indicators
  - Product diversification metrics

-->  the processed dataset is available in a google drive and this is the link : [https://drive.google.com/drive/folders/1BFvHJEyVUSiJkSVXvFMWl3JcJCvCXHlt?usp=sharing](https://drive.google.com/file/d/1DLtei_Q8FUYQHyka7-QuGewcoT6kQF3Q/view?usp=sharing)

### Step 3 : Model Development

**Clustering**
- Group countries by import demand patterns
- Cluster products by global demand trends
- Identify similar export markets

**Classification**
- Label country-product pairs as: High / Medium / Low export opportunity

**Forecasting**
- Predict future trade volume and value trends
- Forecast demand for specific products and sectors

### Step 4 : Evaluation

| Task | Metrics |
|------|---------|
| Forecasting | MAE, RMSE, MAPE |
| Classification | Accuracy, Precision, Recall, F1-score |
| Clustering | Silhouette Score, Davies-Bouldin Index |

---

##  Getting Started:

### Prerequisites

```
Python 3.8+
```

### Installation

```bash
git clone https://github.com/your-username/algerian-export-opportunities.git
cd algerian-export-opportunities
pip install -r requirements.txt
```

### Run the Notebooks

```bash
jupyter notebook notebooks/
```

### Launch the Dashboard

```bash
# Start the data pipeline
python dashboard/pipeline.py

# Then open Grafana and import the dashboard config from dashboard/grafana/
```

---

##  Dashboard:

An interactive dashboard (built with **Grafana** or Apache Superset / Metabase) allows stakeholders to:

- Explore export opportunities by country, sector, and product
- Visualize global demand trends and trade flows
- Monitor predicted export growth and market potential
- Identify priority international markets for Algerian exporters
- Compare historical vs. forecasted trade indicators

---

##  Success Criteria:

- Correctly identify promising international markets for Algerian exporters
- Discover high-demand global products aligned with Algerian export potential
- Provide accurate and interpretable trade forecasts
- Produce meaningful clusters of countries and sectors
- Deliver actionable insights for CACI and export-support institutions
- Strong model performance across multiple sectors and datasets

---

##  Deliverables:

- Integrated multi-source international trade dataset (at least 2 sources)
- Documented Jupyter notebooks (preprocessing, feature engineering, modeling)
- ML models for clustering, classification, and forecasting
- Export opportunity ranking system (by country, product, and sector)
- Interactive visualization dashboard
- Deployed data pipeline connected to the dashboard
- Final technical report and live system demonstration

---

##  Limitations & Future Work:

- Data availability and granularity may vary across sources
- Trade opportunity scores are based on historical patterns and may not reflect geopolitical shifts
- Future: integrate real-time trade data APIs and NLP for trade policy analysis

---



*ENSIA — Machine Learning Project, Spring 2025–2026*

---

##  License:

This project is for academic purposes only.
