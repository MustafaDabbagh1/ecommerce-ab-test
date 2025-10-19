# Project: Retail A/B Test – New Checkout

**Goal:** Measure the impact of a new checkout flow on conversion and average order value (AOV).

**Dataset:** Synthetic sample (100 rows) mirroring the real schema. See `data/schema.json`.

**Stack:** SQL (BigQuery-style), Python (pandas, numpy, matplotlib), Jupyter.

## Quick Start
```bash
pip install -r requirements.txt
jupyter notebook analysis.ipynb


## Files
- `analysis.ipynb — EDA, metrics, hypothesis test, recommendation.
- `squeries.sql — Core tables/metrics and test-ready extracts.
- `sample.csv — Tiny, anonymized sample with the same columns.
- `schema.json — Column names, types, and notes.
- `dashboard.png — Chart exported from the notebook.

## Results (TL;DR)
- **+18.23% absolute lift** in conversion (test worse than control).
- No significant change in AOV (example).
- Statistically significant: z = 2.37, p = 0.0089.
- **Recommendation:** Do not roll out the new checkout. Pause and investigate drivers of the drop (traffic mix, implementation bugs, device/OS splits, and guardrails like bounce rate & page speed). Re-run with tighter instrumentation.

## Reproduce
- Open analysis.ipynb and run all cells.
- Data used in the notebook:
https://raw.githubusercontent.com/MustafaDabbagh1/ecommerce-ab-test/main/sample.csv


## Open Notebook

Nbviewer (fast render): https://nbviewer.org/github/MustafaDabbagh1/ecommerce-ab-test/blob/main/analysis.ipynb

Colab (run in cloud): https://colab.research.google.com/github/MustafaDabbagh1/ecommerce-ab-test/blob/main/analysis.ipynb


```Then click **Commit changes**.
::contentReference[oaicite:0]{index=0}
