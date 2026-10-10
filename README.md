# ECON 3916 Problem Set 1 — The Cost of Living Brief

This project builds a household-specific cost-of-living index for a Boston single parent who rents, drives to work, and supports one school-aged child. The notebook compares the household's fixed 2019 basket with official FRED price series through 2024. Its code intentionally builds on ECON 3916 Labs 2–4: Lab 2's FRED loader, functions, annual-average rebasing and checks; Lab 3's labeled `fig, ax` charts and saved figures; and Lab 4's dictionaries, summary tables, sensitivity thinking, and explicit verification.

## Files

- `Econ_3916_PS1.ipynb` — Colab-compatible notebook containing all five phases
- `README.md` — project summary and submission notes

## What the notebook does

1. Defines a seven-category monthly household basket whose weights sum to 1.0.
2. Implements a base-weighted Laspeyres index and compares it with an unweighted average.
3. Retrieves headline CPI and seven component proxies from FRED, optionally using a personal API key, and rebases all series to 2019 = 100.
4. Audits every series for coverage, frequency, and missing months.
5. Compares own-history estimates with a common-sample estimate.
6. Compares seasonally adjusted and unadjusted headline CPI.
7. Sweeps each household weight from 0 to 0.5, verifies the sensitivity calculation, and identifies which assumption matters most.
8. Generates a director-facing finding of no more than 250 words from the calculated results.

## Running in Colab

Open the notebook in Google Colab and choose **Runtime → Run all**. The data cells require internet access. A FRED API key may be pasted into the clearly marked `FRED_API_KEY` cell; leaving it blank uses FRED's public CSV endpoint. Never commit a real API key to a public repository.

## Important Phase 4 requirement

The notebook contains a clearly marked transcript placeholder. Before submission, the student must run the required P.R.I.M.E. prompt and paste the actual prompt and model reply exactly as sent and returned, along with the real model name and date. A reconstructed transcript does not meet the assignment requirement.

## Main limitation

This is one transparent household scenario, not a survey of the employer's workers. The official proxies are national series and cannot capture every Boston lease, benefit, subsidy, shopping choice, or commuting arrangement. The sensitivity analysis shows how conclusions change when spending shares differ.
