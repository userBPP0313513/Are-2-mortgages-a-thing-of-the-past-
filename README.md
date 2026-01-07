# Are 2% Mortgages a Thing of the Past?

This project explores whether UK two-year fixed mortgage rates around **2%**
are likely to return, using time-series analysis of mortgage rates, the
Bank of England base rate, and CPI inflation.

The analysis focuses on the post-2016 period, when consistent overlap
across datasets is strongest, and applies exploratory analysis, lag
relationships, and baseline forecasting to assess whether ultra-low
mortgage rates are likely to re-emerge.

---

## Key Question
**Are 2% two-year fixed mortgages likely to return under current monetary conditions?**

---

## Data & Scope
The analysis uses monthly UK data for:

- Two-year fixed mortgage rates  
- Bank of England base rate  
- CPI inflation (12-month rate)  

All series are:
- Aligned to **month-end frequency**
- Restricted to **2016 onwards** for consistency

---

## Analytical Approach
1. Data cleaning and monthly alignment (ETL)
2. Time-series visualisation
3. Trend smoothing using rolling averages
4. Correlation and lag analysis
5. Baseline ARIMA forecasting and back-testing
6. Interpretation and conclusions

---

## Key Findings
- Mortgage rates move closely with the Bank of England base rate.
- Lag analysis suggests mortgage rates typically respond within **1–3 months**.
- Inflation shows a weaker direct relationship with mortgage rates.
- Forecasting suggests some easing is possible, but a sustained return to
  **~2% mortgage rates appears unlikely** without a major shift in monetary policy.

---

## Conclusion
**2% mortgages appear to be a feature of a specific low-rate economic era
rather than a baseline expectation going forward.**

While not permanently impossible, their return would likely require a
prolonged period of materially lower interest rates and stable inflation,
similar to conditions observed prior to 2022.

---

## Repository Structure
ARE-2-MORTGAGES-A-THING-OF-THE-PAST-/
├── Data/
│   ├── RAW/
│   └── Processed/
│       ├── bank_rate_clean.csv
│       ├── cpi_clean.csv
│       └── mortgage_clean.csv
├── Notebooks/
│   ├── 01_experimental.ipynb
│   └── 02_analysis_final.ipynb
├── .gitignore
└── README.md

---

## Notebooks
- **`Notebooks/02_analysis_final.ipynb`**  
  The main, fully-structured analysis answering the project question.
  This is the recommended starting point.

- **`Notebooks/01_experimental.ipynb`**  
  Exploratory and experimental work used during development.  
  Included for transparency, but not intended as a polished narrative.

---

## How to Run
1. Clone the repository
2. Install Python dependencies:
   - pandas
   - matplotlib
   - statsmodels
   - scikit-learn
3. Open `Notebooks/02_analysis_final.ipynb`
4. Run all cells top-to-bottom

---

## Notes & Limitations
- Forecasting models are univariate and do not include exogenous predictors.
- Structural breaks (e.g. post-2022) limit long-horizon forecasting accuracy.
- Results are analytical and illustrative, not financial advice.

---

## Tech Stack
Python, pandas, matplotlib, statsmodels, scikit-learn
