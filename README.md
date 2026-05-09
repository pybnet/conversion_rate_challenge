# Conversion Rate Challenge

Predict whether a user will subscribe to a newsletter based on behavioral and demographic data.

## Dataset

284,580 entries — 5 features + 1 target (`converted`)

| Feature | Type | Description |
|---|---|---|
| `country` | categorical | User's country |
| `age` | numerical | User's age |
| `new_user` | numerical | 1 = new user, 0 = returning |
| `source` | categorical | Traffic source (Ads, Seo, Direct) |
| `total_pages_visited` | numerical | Pages visited during session |

## Model

Random Forest — `max_depth=10`, `min_samples_leaf=5`

| Metric | Train | Test |
|---|---|---|
| F1-score | 0.774 | 0.759 |
| Precision | 0.87 | 0.85 |
| Recall | 0.70 | 0.68 |

## Key Findings

- `total_pages_visited` is by far the strongest predictor (88.6% importance)
- Returning users convert 2x more than new users
- Germany and UK have the highest conversion rates (6.2%, 5.2%)
- Traffic source has negligible impact on conversion