# Customer Analytics, Segmentation & Price Elasticity Modelling

An end-to-end retail customer-analytics pipeline: segment customers from demographic data, profile how each segment actually shops, then model purchase probability, brand choice, and price elasticity at the segment level to support targeted pricing and promotion decisions.

---

## What this answers

Retailers don't want one price or one promotion for everyone — they want to know *which customers* respond to price and which don't. This project builds that, in three steps: find the segments, describe their behaviour, then quantify how each one reacts to price.

## Data

Two retail datasets (committed under `data/`):
- **Segmentation data** — 2,000 customers with 7 demographic features (sex, marital status, age, education, income, occupation, settlement size).
- **Purchase data** — transaction-level records (brand choices, prices, promotions, quantities) used for the behavioural and elasticity models.

## Pipeline

| Notebook | What it does |
|---|---|
| `01_Segmentation.ipynb` | EDA, standardisation, PCA, K-Means clustering into segments |
| `02_Descriptive_Analysis.ipynb` | Assigns segments to purchase data, profiles purchase incidence, spend and brand behaviour |
| `03_Modelling.ipynb` | Purchase-probability, brand-choice and quantity models; own/cross price elasticity; promotion effects |

The trained `scaler`, `pca`, and `kmeans` models are saved in `models/` and reloaded in notebooks 02–03, so every customer is assigned to a segment consistently across the whole project.

## Approach

**Segmentation.** Features are standardised (essential before distance-based clustering), reduced with PCA, then clustered with K-Means into **4 segments** (proportions ≈ 29% / 36% / 15% / 20%). Segments are profiled by income, occupation, and settlement size to give each a behavioural identity.

**Behavioural profiling.** Each segment's purchase incidence, average spend, and brand mix are compared — separating active buyers from browsers, which is what decides where promotional budget should go.

**Price elasticity.** A logistic purchase-probability model gives the price coefficient, from which price elasticity is computed (`PE = β × price × (1 − P)`) overall and per segment. A linear model handles purchase quantity, and brand choice is modelled to derive own- and cross-price elasticities.

## Key findings

- Four behaviourally distinct segments, unevenly sized (the largest ≈ 36%, the smallest ≈ 15%).
- Price elasticities are **negative across all segments** (everyone is price-sensitive to some degree), but the **magnitude differs by segment** — so price sensitivity is segment-specific, not uniform.
- That difference is the actionable result: less price-sensitive segments can sustain premium pricing / lighter discounting, while more elastic segments are where promotions move the needle.

## Run it

```bash
git clone https://github.com/manzoor-syiemlieh/customer-analytics-segmentation.git
cd customer-analytics-segmentation
# run the notebooks in order 01 -> 03; the data is included under data/
```

## Tools

Python · Pandas · NumPy · Scikit-learn · SciPy · Matplotlib · Seaborn

## Author

**Manzoor Syiemlieh** — Fraud & Risk Analytics, 7+ years (PayPal) → Data Science
[LinkedIn](https://www.linkedin.com/in/manzoor-syiemlieh-4193683a5/) ·
[GitHub](https://github.com/manzoor-syiemlieh)

MIT Licensed.
