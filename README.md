# 🏀 NBA MVP Prediction

A machine learning project that predicts the **NBA Most Valuable Player (MVP)** for each season using historical player and team statistics. Built as a Diploma Final Year Project (FYP), it covers the full data science pipeline, from web scraping to an interactive Streamlit UI.

---

## 📁 Project Structure

```
NBA_MVP_Prediction_FYP/
│
├── FYP_web_scraping.ipynb          # Scrapes player, team & MVP data from the web
├── FYP_data_cleaning.ipynb         # Cleans and merges raw data into a usable format
├── FYP_EDA_visualizations.ipynb    # Exploratory data analysis & visualizations
├── FYP_PredictionModels.ipynb      # ML model training, evaluation & prediction
├── FYP_DataShowcasingInterface.ipynb # Streamlit interface for browsing processed data
├── FYP_Prediction_UI.ipynb         # Streamlit interface for viewing MVP predictions
│
├── players.csv                     # Raw player stats (1995–2023)
├── teams.csv                       # Raw team win/loss records (1995–2023)
├── mvps.csv                        # Historical MVP winners (1995–2023)
├── players_mvp_stats.csv           # Cleaned & merged dataset for modelling
├── all_predictions_final.csv       # Model output used by the prediction UI
└── nicknames.txt                   # Player nickname mappings for name normalization
```

---

## ⚙️ Pipeline Overview

### 1. Web Scraping — `FYP_web_scraping.ipynb`
Scrapes historical player stats, team records, and MVP award data covering NBA seasons from 1995 to 2023.

### 2. Data Cleaning — `FYP_data_cleaning.ipynb`
Handles missing values, normalizes player names (using `nicknames.txt`), and merges player stats with team performance data and MVP labels into `players_mvp_stats.csv`.

### 3. EDA — `FYP_EDA_visualizations.ipynb`
Explores key patterns in the data: stat distributions, correlations with MVP votes, and trends over the years.

### 4. Prediction Models — `FYP_PredictionModels.ipynb`
Trains and evaluates machine learning models to predict the MVP for each season. Generates `all_predictions_final.csv` for the UI.

### 5. Streamlit UIs
- **`FYP_DataShowcasingInterface.ipynb`** — Browse the processed player and team data interactively
- **`FYP_Prediction_UI.ipynb`** — View season-by-season MVP predictions from the trained models

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook
- Streamlit

### Installation

```bash
git clone https://github.com/yungxuan819/NBA_MVP_Prediction_FYP.git
cd NBA_MVP_Prediction_FYP
pip install pandas numpy scikit-learn matplotlib seaborn streamlit requests beautifulsoup4
```

### Run the Notebooks (in order)

```
1. FYP_web_scraping.ipynb
2. FYP_data_cleaning.ipynb
3. FYP_EDA_visualizations.ipynb
4. FYP_PredictionModels.ipynb
```

### Launch the UI

Convert and run either Streamlit notebook:

```bash
jupyter nbconvert --to script FYP_Prediction_UI.ipynb
streamlit run FYP_Prediction_UI.py
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| BeautifulSoup / Requests | Web scraping |
| pandas | Data cleaning & manipulation |
| scikit-learn | Machine learning models |
| matplotlib / seaborn | EDA visualizations |
| Streamlit | Interactive UI |
| Jupyter Notebook | Development environment |

---

## 📊 Data Coverage

- **Seasons:** 1995 – 2023
- **Sources:** Player per-game stats, team win/loss records, MVP voting results
- **Scope:** All players who received MVP votes across covered seasons
