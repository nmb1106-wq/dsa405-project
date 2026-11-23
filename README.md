# DSA 405: Risk Disclosures and Stock Returns (Fall 2026)

This five-company pilot asks whether year-over-year changes in SEC 10-K Item 1A risk-factor length relate to subsequent 12-month stock-price returns. Across **23 complete pairs**, the Pearson correlation was **−0.236**; excluding the unusually large Abbott 2022 risk-length increase, it was **+0.184** across 22 pairs. The relationship is weak and sensitive to one observation, so it does not support a reliable predictive conclusion.

## Sources and permissions
- [Wikipedia current S&P 500 constituent table](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies), public page (CC BY-SA terms generally apply): ticker, company and CIK identifiers; **not historical membership**.
- [SEC EDGAR](https://www.sec.gov/edgar), public 10-K filings and submissions metadata, subject to [fair-access guidance](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data).
- [WRDS / CRSP Stock Version 2 (CIZ)](https://wrds-www.wharton.upenn.edu/), **licensed** daily security data, accessed through authorized university access. Do not publish raw or derived daily CRSP prices without permission.

## Reproduce
1. Install Python and `pip install -r requirements.txt`.
2. Open `DSA405_002_FA26_P3_nmbrockm.ipynb` in Colab or Jupyter and work from the repository root.
3. Authorized WRDS users: download CRSP CIZ daily data for ABT, AAPL, A, ABBV, ABNB, 2019-01-01 through 2025-12-31, and construct the split-adjusted price file `data/raw/approved_daily_prices.csv` with columns `ticker,date,adjusted_close`. Validate the adjustment-factor conversion against CRSP documentation. The file is intentionally not included in public repository materials.
4. Run acquisition, risk extraction, price import, join, and verification cells in order. The notebook now prompts for the licensed CSV before the price-import cell if the file is absent in Colab. In Jupyter, place the file under `data/raw/` before running. The optional Google Drive mount and premature diagnostics have been removed.
5. Check outputs: 28 filings, 8,310 daily price records, 23 complete analysis pairs, full-sample correlation −0.236, and correlation +0.184 without Abbott 2022. SEC/Wikipedia changes may affect reproducibility.

## Files
- `DSA405_002_FA26_P1_nmbrockm.ipynb` — framing
- `DSA405_002_FA26_P2_nmbrockm.ipynb` — constituent cleaning
- `DSA405_002_FA26_P3_nmbrockm.ipynb` — acquisition, integration and checks
- `P4_Project_Synthesis_Report.md` and `.docx` — written report and rubric
- `data/raw/` — locally downloaded inputs (licensed CRSP file excluded)
- `data/processed/` — locally generated intermediate outputs

**Remaining checks:** validate more SEC extraction boundaries (especially Abbott 2022), confirm CRSP split adjustments, test a clean notebook run, and verify the final GitHub URL. Do not commit credentials.

## Submission and validation status
The P4 written report includes the seven-criterion provisional self-scored rubric. Moodle requires the repo URL, notebook and report. **The notebook has not been verified with a full fresh-kernel run after this packaging update.** Run it with an authorized local CRSP CSV, verify the Abbott extraction and CRSP price-adjustment conversion, and update the repo URL before submitting.
