# India-Stocks-1651-1680-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1651 to 1680)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1651-1680-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1651 to 1680)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1651 | `MGEL` | Mangalam Global Enterprise Limited | `MGEL.NS` |
| 1652 | `MHLXMIRU` | Mahalaxmi Rubtech Limited | `MHLXMIRU.NS` |
| 1653 | `MHRIL` | Mahindra Holidays & Resorts India Limited | `MHRIL.NS` |
| 1654 | `MICEL` | MIC Electronics Limited | `MICEL.NS` |
| 1655 | `MIDHANI` | Mishra Dhatu Nigam Limited | `MIDHANI.NS` |
| 1656 | `MIDWESTLTD` | Midwest Limited | `MIDWESTLTD.NS` |
| 1657 | `MIIL` | Meghna Infracon Infrastructure Limited | `MIIL.NS` |
| 1658 | `MILKYMIST` | Milky Mist Dairy Food Limited | `MILKYMIST.NS` |
| 1659 | `MINALIND` | Minal Industries Limited | `MINALIND.NS` |
| 1660 | `MINDTECK` | Mindteck (India) Limited | `MINDTECK.NS` |
| 1661 | `MIRZAINT` | Mirza International Limited | `MIRZAINT.NS` |
| 1662 | `MITCON` | MITCON Consultancy & Engineering Services Limited | `MITCON.NS` |
| 1663 | `MITTAL` | Mittal Life Style Limited | `MITTAL.NS` |
| 1664 | `MKEXIM` | M.K. Exim (India) Limited | `MKEXIM.NS` |
| 1665 | `MKPL` | M K Proteins Limited | `MKPL.NS` |
| 1666 | `MLKFOOD` | Milkfood Limited | `MLKFOOD.NS` |
| 1667 | `MMFL` | MM Forgings Limited | `MMFL.NS` |
| 1668 | `MMP` | MMP Industries Limited | `MMP.NS` |
| 1669 | `MMWL` | Media Matrix Worldwide Limited | `MMWL.NS` |
| 1670 | `MOBIKWIK` | One Mobikwik Systems Limited | `MOBIKWIK.NS` |
| 1671 | `MODINATUR` | Modi Naturals Limited | `MODINATUR.NS` |
| 1672 | `MODIRUBBER` | Modi Rubber Limited | `MODIRUBBER.NS` |
| 1673 | `MODIS` | Modis Navnirman Limited | `MODIS.NS` |
| 1674 | `MODISONLTD` | MODISON LIMITED | `MODISONLTD.NS` |
| 1675 | `MODTHREAD` | Modern Threads (India) Limited | `MODTHREAD.NS` |
| 1676 | `MOHITE` | Mohite Industries Limited | `MOHITE.NS` |
| 1677 | `MOHITIND` | Mohit Industries Limited | `MOHITIND.NS` |
| 1678 | `MOIL` | MOIL Limited | `MOIL.NS` |
| 1679 | `MOKSH` | Moksh Ornaments Limited | `MOKSH.NS` |
| 1680 | `MOL` | Meghmani Organics Limited | `MOL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream MGEL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1651-1680-Historical-Data/main/MGEL/1m/2026/10/MGEL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
