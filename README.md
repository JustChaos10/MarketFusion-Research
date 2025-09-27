# MarketFusion Research

A notebook-driven research stack for equities and mutual funds that blends **news analytics**, **value analysis**, and **fund screening** into one workflow. It includes exploratory notebooks, lightweight data caches (CSV/PKL), and an optional trade/practice notebook. *For research and education only.*

> ⚠️ **Disclaimer**: Past performance does not predict future results; backtests are prone to overfitting and data-snooping biases. Use findings cautiously and never as financial advice.

---

## 📁 Project map

- `news_analysis.ipynb` — build/inspect news features (e.g., sentiment) and join with tickers. Uses `news_.pkl` if provided.
- `mutual_funds.ipynb` — explore mutual fund metrics and screening. Uses `mf_saved.csv`.
- `value_analysis.ipynb` — value & fundamentals checks for equities. May use `stocks_saved.csv`.
- `trade_platform.ipynb` — simple trade/practice workflow for experimentation (paper only).
- `integrated.ipynb` — tie components together for end‑to‑end feature -> screen -> review.
- `final.ipynb` — a cleaned, rerunnable version of the integrated workflow.

**Data files (examples):**
- `mf_saved.csv`, `stocks_saved.csv`, `tick_final.csv` — cached tabular data.
- `news_.pkl` — serialized news dataset or feature store.
- `tickers.numbers` — personal watchlist (Apple Numbers format).

> If your local files live elsewhere, set the correct paths in the notebooks under the *Parameters / Config* cell.

---

## 🚀 Quickstart

### 1) Create a virtual environment
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
# source venv/bin/activate
```

### 2) Install dependencies
If you have a `requirements.txt`:
```bash
pip install -r requirements.txt
```
Otherwise, install what your notebooks use (typical):
```bash
pip install pandas numpy matplotlib scikit-learn jupyter ipykernel
```

### 3) Make the venv selectable in Jupyter
```bash
python -m ipykernel install --user --name marketfusion-venv --display-name "Python (marketfusion)"
```
Then open the notebooks and choose the **Python (marketfusion)** kernel.

---

## ▶️ Running the notebooks

1. Launch Jupyter:
   ```bash
   jupyter notebook
   # or
   jupyter lab
   ```
2. Open each notebook in order (e.g., `news_analysis.ipynb` → `value_analysis.ipynb` → `mutual_funds.ipynb` → `integrated.ipynb`).
3. Set any paths/api keys in the first config cell.
4. **Run All** and inspect outputs (plots, tables, exports).

> Tip: For repeatable runs, consider parameterizing notebooks with tools like **papermill**, or converting to scripts with **nbconvert/jupytext**.

---

## ⚠️ Research caveats

- **Past performance** does not predict future results.
- **Backtests** are susceptible to **overfitting** and **data snooping** when many variants are tried.
- **Paper trading** results often diverge from live execution due to latency, slippage, and market impact.
- Treat outputs as **exploration**, not investment advice.
---

## 🙌 Credits

Built with Python & Jupyter. Data sources and news processing are user‑provided; plug in your own datasets and APIs.
