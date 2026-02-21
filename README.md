<div align="center">

<img src="https://img.shields.io/badge/S%26P%20500-Analysis%20Project-blue?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xNiA2bDIuMjkgMi4yOS00LjE3IDQuMTctNCA0LTQuNTktNC41OUw0IDEzbDYgNiA0LTQgNC40Mi00LjQyTDIwIDEyVjZoLTR6Ii8+PC9zdmc+" alt="S&P 500 Analysis"/>

# 📈 S&P 500 Analysis Project

### *Decoding the Market — From Raw Data to Real Insights*

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Excel](https://img.shields.io/badge/Microsoft-Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)](https://microsoft.com/excel)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://kaggle.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/ABDELAALI-ENNAMAT/S-P-500-Analysis-Project?style=flat-square&color=gold)](https://github.com/ABDELAALI-ENNAMAT/S-P-500-Analysis-Project/stargazers)

<br/>

> **"The stock market is a device for transferring money from the impatient to the patient."**  
> — *Warren Buffett*

</div>

---

## 🌟 Project Overview

The **S&P 500** (Standard & Poor's 500) is the heartbeat of the U.S. economy — a market index tracking the performance of **500 of the largest publicly traded companies** in the United States. This project dives deep into over **a decade of market data** to uncover trends, growth patterns, and actionable investment insights.

From raw data ingestion and thorough cleaning in **Python (Pandas)**, to interactive visualizations in **Microsoft Excel** with Power Query and pivot tables — this end-to-end analysis transforms millions of data points into clear, compelling intelligence.

---

## 📁 Repository Structure

```
📦 S-P-500-Analysis-Project
├── 📓 S&P500.ipynb                  ← Full Python analysis notebook
├── 📂 Python Cleaned Data/
│   ├── 📄 Stocks.csv                ← Historical stock data (1.8M+ rows)
│   ├── 📄 Index.csv                 ← S&P 500 index history
│   ├── 📄 Index_Monthly.csv         ← Monthly index aggregates
│   ├── 📄 Index_Year.csv            ← Yearly index aggregates
│   └── 📄 Companies.csv             ← 503 company profiles
├── 📂 Dashboard Images/             ← Excel dashboard screenshots
└── 📄 README.md
```

---

## 📊 The Data Universe

Three richly detailed datasets power this analysis:

| Dataset | Rows | Key Columns | Description |
|---------|------|-------------|-------------|
| 📈 **Stocks** | 1,830,417 | `date`, `symbol`, `adjclose`, `high`, `low`, `open`, `volume` | Daily OHLCV data for 503 companies |
| 📉 **Index** | 2,517 | `date`, `S&P500` | Historical S&P 500 index values |
| 🏢 **Companies** | 503 | `sector`, `industry`, `marketcap`, `ebitda`, `revenuegrowth`, `fulltimeemployees`, ... | Fundamental & geographic company data |

> 📦 **Dataset Source:** Imported directly from Kaggle via the Kaggle Python API.

---

## 🎯 Project Objectives

This project was built to answer the most pressing investor questions:

- 📐 **CAGR Calculation** — Measure the Compound Annual Growth Rate of the index and individual stocks
- 🏆 **Outperformers** — Identify companies beating the market benchmark of **10.8% CAGR**
- 💡 **Best Investments** — Surface the top historical investment opportunities
- 🏭 **Sector & Industry Analysis** — Pinpoint which sectors drive the most growth
- 👥 **Employment Leaders** — Discover who employs the most people in America
- 💰 **Market Cap & Revenue** — Rank companies by financial firepower
- 🌍 **Geographic Distribution** — Map where S&P 500 companies call home

---

## 🛠️ Methodology & Workflow

### 1️⃣ Data Import
Data was pulled directly from Kaggle using the **Kaggle Python API**, ensuring reproducibility and access to the latest dataset versions.

### 2️⃣ Data Cleaning (Python / Pandas)

Rigorous cleaning was applied to guarantee data quality:

| Issue | Dataset | Solution Applied |
|-------|---------|-----------------|
| Null stock rows | Stocks | Dropped records for companies listed **after** Jan 4, 2010 |
| Missing `revenuegrowth` | Companies | Imputed using **mean % change** of `adjclose` |
| 29 missing `ebitda` values | Companies | Filled with **sector median** (Financial Services) |
| 19 missing `state` values | Companies | **Manually researched** by corresponding city |
| 4 missing `fulltimeemployees` | Companies | Sourced from **reliable public references** |

### 3️⃣ Analysis Pipeline
1. Computed **CAGR** for the S&P 500 index and all individual stocks
2. Filtered to only stocks listed for **10+ years** (469 companies)
3. Segmented analysis by **sector, industry, and geography**
4. Deep-dived into **Tesla, NVIDIA, and Broadcom Inc.**
5. Aggregated data to **monthly and yearly** granularities

### 4️⃣ Visualization (Excel + Power Query)
- Imported cleaned CSVs into Excel via **Power Query**
- Built **Pivot Tables** across all three datasets
- Designed a multi-sheet **interactive Excel dashboard** with charts covering index trends, top performers, sector breakdowns, employment, and more

---

## 🔍 Key Findings & Observations

### 📉 Index Performance

| Metric | Value |
|--------|-------|
| 📊 CAGR (2010–2023) | **10.8%** |
| 🟢 Best Year | **2021** (+1,010 pts) |
| 🔴 Worst Year | **2022** (−922 pts) |
| 💉 COVID Crash | **March 2020** (−19%) |
| 💪 COVID Recovery | **June 2020** (+6.3%) |
| 🚀 Post-COVID Bounce | **2023** (+930 pts) |

### 🏆 Top Stock Performers (10+ Year CAGR)

| Rank | Company | CAGR | Notable Trait |
|------|---------|------|---------------|
| 🥇 | **NVIDIA** | **49%** | AI & GPU Dominance |
| 🥈 | **Tesla** | **40%** | EV Pioneer |
| 🥈 | **Broadcom Inc.** | **40%** | Semiconductor Giant |

> ⚠️ **Tesla** exhibited the highest **volatility** of any top performer, with dramatic swings in recent years.

### 🏢 Company Landscape

| Category | Leaders |
|----------|---------|
| 👥 **Top Employers** | Walmart, Amazon, Accenture |
| 💎 **Largest Market Cap** | NVIDIA, Microsoft, Apple |
| 🚀 **Fastest Revenue Growth** | NVIDIA, Super Micro Computer, Blackstone |
| 💸 **Most Expensive Stock** | NVR, Inc. |
| 🏭 **Best Performing Sectors** | Technology, Consumer Discretionary |

### 🏭 Fastest-Growing Industries

> Rental & Leasing Services · Trucking · Consumer Electronics  
> *Multi-company leaders:* **Software — Application** & **Semiconductors**

---

## 💡 Investment Insights

```
📌 S&P 500 CAGR Benchmark:  10.8%
🏆 Top Picks (Historical):  NVIDIA · Broadcom Inc.
📈 Hot Industries:           Semiconductors · Software · Consumer Electronics
🌍 Market Reach:             U.S.-dominated with global operations
```

- The index has demonstrated **consistent, resilient growth** over a decade, rebounding from crises (COVID-19, 2022 correction)
- **NVIDIA** stands as the runaway leader — driven by the AI revolution — with a jaw-dropping **49% CAGR**
- **Diversifying across Semiconductor and Software** companies provides the best risk-adjusted growth profile
- Even in bear years (2022), long-term investors who held were rewarded by the 2023 recovery

---

## 🖥️ Dashboard Preview

> The Excel dashboard translates all of this analysis into a clean, interactive experience. Screenshots are available in the [`Dashboard Images/`](./Dashboard%20Images/) folder.

### 🧪 Test the Dashboard Yourself

Want to interact with the full Excel dashboard? Follow these steps:

1. **⬇️ Download the Dataset**  
   > 🔗 *Kaggle link coming soon — will be added here to allow you to download the Excel file directly.*  
   > Once available, download the `.xlsx` file from the Kaggle dataset page.

2. **📂 Open in Microsoft Excel**  
   Open the downloaded `.xlsx` file in **Microsoft Excel 2016 or later** (Power Query support required).

3. **🔄 Refresh Power Query**  
   Go to `Data → Refresh All` to reload data connections if prompted.

4. **🗂️ Navigate the Sheets**  
   The workbook contains multiple sheets:
   - `Index Dashboard` — S&P 500 trend lines, yearly & monthly breakdown
   - `Stocks Dashboard` — Top performers, CAGR rankings, Tesla/NVIDIA/Broadcom deep-dives
   - `Companies Dashboard` — Sector analysis, market cap, revenue growth, employment, geography

5. **🎛️ Use Slicers & Filters**  
   Interact with the pivot slicers to filter by **sector**, **year**, **country**, and more.

6. **📸 Compare with Screenshots**  
   Cross-reference with the images in [`Dashboard Images/`](./Dashboard%20Images/) to verify your setup matches the expected output.

> ✅ **Recommended:** Use Excel desktop for the best experience. Google Sheets may not support all Power Query features.

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| 🐍 **Python 3.x** | Data ingestion, cleaning, and analysis |
| 📓 **Jupyter Notebook** | Interactive development environment |
| 🐼 **Pandas** | Data manipulation and transformation |
| 📦 **Kaggle API** | Dataset retrieval |
| 📊 **Microsoft Excel** | Dashboard creation and visualization |
| ⚡ **Power Query** | Data transformation within Excel |
| 🔢 **Pivot Tables** | Multi-dimensional data aggregation |

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas kaggle jupyter
```

### Run the Notebook

```bash
# Clone the repository
git clone https://github.com/ABDELAALI-ENNAMAT/S-P-500-Analysis-Project.git
cd S-P-500-Analysis-Project

# Launch Jupyter
jupyter notebook "S&P500.ipynb"
```

### Kaggle API Setup

```bash
# Place your kaggle.json credentials at ~/.kaggle/kaggle.json
# Then datasets will auto-download when the notebook is run
```

---

## 📂 Cleaned Data Files

| File | Description |
|------|-------------|
| `Stocks.csv` | Cleaned daily OHLCV data for 503 stocks |
| `Index.csv` | Daily S&P 500 index values |
| `Index_Monthly.csv` | Monthly aggregated index performance |
| `Index_Year.csv` | Yearly aggregated index performance |
| `Companies.csv` | Full company fundamentals & metadata |

> 📝 All files are stored via **Git LFS** due to their large size.

---

## 🤝 Contributing

Contributions, ideas, and feedback are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-idea`
3. Commit your changes: `git commit -m "Add: your feature"`
4. Push to the branch: `git push origin feature/your-idea`
5. Open a Pull Request 🎉

---

## 👤 Author

<div align="center">

**Abdelaali Ennamat**

[![GitHub](https://img.shields.io/badge/GitHub-ABDELAALI--ENNAMAT-181717?style=for-the-badge&logo=github)](https://github.com/ABDELAALI-ENNAMAT)

*Data Analyst passionate about turning raw numbers into actionable insights.*

</div>

---

## 📜 License

This project is licensed under the **MIT License** — feel free to use, share, and build upon it.

---

<div align="center">

⭐ **If this project helped you, please give it a star!** ⭐

*Made with ❤️ and lots of data by Abdelaali Ennamat*

</div>