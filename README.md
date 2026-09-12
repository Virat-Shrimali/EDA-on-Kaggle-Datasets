# EDA on Kaggle Datasets

This repository contains exploratory data analysis (EDA) work on Kaggle-style tabular datasets, organized by dataset-specific subdirectories.

## Repository Structure

- `heart_disease/`
  - `heart.csv`: Heart disease dataset (918 rows, 12 columns).
  - `EDA_heart_disease.ipynb`: Main EDA notebook with data inspection, cleaning, visualization, encoding, scaling, and correlation checks.
  - `.gitkeep`: Placeholder file.
- `insurance/`
  - `insurance.csv`: Medical insurance dataset (1338 rows, 7 columns).
  - `EDA_insurance.ipynb`: Notebook scaffold with Colab link (currently no analysis cells).
  - `.gitkeep`: Placeholder file.
- `heart.csv`
  - A root-level copy of the same heart disease dataset used in `heart_disease/`.

## Dataset Details

### 1) Heart Disease Dataset (`heart_disease/heart.csv`)
- Columns: `Age`, `Sex`, `ChestPainType`, `RestingBP`, `Cholesterol`, `FastingBS`, `RestingECG`, `MaxHR`, `ExerciseAngina`, `Oldpeak`, `ST_Slope`, `HeartDisease`
- Target variable: `HeartDisease` (binary)
- Source: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

### 2) Insurance Dataset (`insurance/insurance.csv`)
- Columns: `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`
- Typical use case: analyzing medical charge patterns against demographic and lifestyle factors.
- Source: https://www.kaggle.com/datasets/mirichoi0218/insurance

## What the Heart Disease Notebook Currently Covers

The notebook `heart_disease/EDA_heart_disease.ipynb` includes:
- Basic inspection (`shape`, `info`, `describe`, duplicates, null checks)
- Target distribution checks (`HeartDisease`)
- Handling invalid zero values in `Cholesterol` and `RestingBP`
- Distribution plots for major numeric features
- Categorical feature analysis with `countplot`
- Comparative plots (box/violin) by heart disease status and sex
- Correlation heatmap for numeric variables
- One-hot encoding (`pd.get_dummies`) and numeric type conversion
- Feature scaling using `StandardScaler`
- Pearson correlation setup for selected features vs target

## How to Use

1. Open notebooks locally in Jupyter or in Google Colab.
2. Start with:
   - `heart_disease/EDA_heart_disease.ipynb` for complete EDA workflow.
   - `insurance/EDA_insurance.ipynb` as a starting point for future insurance EDA.
3. Ensure common Python EDA libraries are available:
   - `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`

## Notes

- The heart disease notebook loads data from the repository's raw GitHub URL in one step; local CSV files are also present.
- The insurance notebook is currently minimal and can be expanded with cleaning, visualization, and statistical analysis similar to the heart disease workflow.
