# DSA 405 Project

## Research Question

Do S&P 500 companies whose 10-K risk factor section (Item 1A) got a lot longer from one year to the next have worse stock returns over the following 12 months than companies whose risk section stayed about the same length?

## Project Overview

This project examines changes in the length of the Risk Factors section of S&P 500 companies' annual 10-K filings and their relationship with subsequent stock returns.

The overall project uses SEC EDGAR 10-K filings for risk-factor information and stock-price data for measuring returns. An S&P 500 constituent dataset provides company identifiers used to connect the sources.

## Project 2

Project 2 audits, cleans, and documents the S&P 500 constituent dataset.

The dataset includes ticker symbols, company names, GICS sectors and sub-industries, headquarters locations, dates added to the S&P 500, SEC CIK identifiers, and founding information.

The original source file is preserved without modification at:

`data/raw/constituents.csv`

Additional source documentation is located at:

`data/raw/SOURCES.md`

## How to Run

1. Open `DSA405_002_FA26_P2_nmbrockm.ipynb` in Google Colab.
2. Run the notebook from top to bottom.
3. The notebook loads the raw S&P 500 constituent dataset from this GitHub repository.
4. It audits the raw data, creates a data dictionary, performs cleaning, documents each cleaning decision, reconciles row and column counts, and validates the cleaned dataset.

The raw data should not be modified directly. All cleaning is performed on a copy of the raw dataset.
