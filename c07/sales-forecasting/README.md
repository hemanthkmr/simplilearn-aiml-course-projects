# Sales Forecasting (Capstone 3) - REPORT

Status: DONE. Notebook `Sales_Forecasting.ipynb` (executed, no errors), `Sales_Forecasting.html`, and `submission/` (Sales_Forecasting.ipynb, Source_Code.zip, Writeup.docx, Screenshots.zip). Data: course 07 Datasets.zip, Capstone 3 (copied to `data/`).

## Steps met
Preliminary analysis (import, shape/structure/outliers, merge into date, item id, price, item count, item name, kcal, store id, store name); EDA a-h (overall, weekday, month, quarter, restaurants by year/month/day, popular items and stores, volume vs money per day, most expensive item with kcal); ML (calendar features, last six months as test, LR / RF / XGBoost RMSE, best model forecast for next year). Extra (grading rubric): LSTM with training series, 12-month recursively generated test series, MAPE, and a 3-month forecast from a model trained on the full series.

## Key metrics (test = Jul-Dec 2021)
| Model | RMSE | MAPE % |
|---|---|---|
| Random Forest (best) | 826.85 | 11.08 |
| XGBoost | 894.98 | 14.56 |
| Seasonal naive (reference) | 967.80 | 11.81 |
| Linear Regression | 2234.61 | 40.57 |
| LSTM recursive 12 months | 2239.32 | 26.93 |
| LSTM one-step 12 months | 727.77 | 10.68 |

Findings: Bob's Diner earns over 99% of revenue (other stores about 1-2 units/day); Q2/Q3 about 50% above Q1/Q4; Thu-Sat strongest; June peak; Random Forest 2022 forecast about 2.38M (about flat vs 2021 because trees cannot extrapolate the year trend).

## Deviations / notes
- "Sales" is defined as revenue = price x item_count (item counts also shown).
- The rubric's LSTM section is not in the problem-statement PDF; added as an extra. LSTM results vary slightly between runs (TensorFlow nondeterminism); the 26.9% / 10.7% figures are from the saved run, and the interpretation text matches them.
- Seasonal-naive baseline added as a sanity reference only.

Run time: about 3.5 to 6 minutes on CPU.
