# Professional Tennis Match Data Analysis

An exploratory data analysis project answering 15 real-world analytical questions about professional tennis matches (ATP & WTA), using a large-scale, multi-table dataset — completed as a project during the Data Analytics Bootcamp at Daneshkar Academy (April–May 2026).

## 🎯 Objective
Explore a large, real-world professional tennis dataset spanning players, matches, in-match statistics, and tournaments, and answer a series of analytical business questions using Python — from simple counts to correlation analysis and outlier-aware duration modeling.

## 🗂️ Dataset
- Multi-table dataset of professional tennis matches (ATP & WTA), originally provided in **Parquet format** and converted to CSV for analysis (see `parquet to csv.ipynb`).
- Key tables: home/away player info (name, height, country, handedness, ranking), match events & results, per-set timing, in-match statistics (aces, double faults, breaks of serve), and tournament metadata (surface type, etc.).
- Due to its large size, the raw data files are not included in this repository — reach out or refer to the original source for access.

## 🛠️ Tech Stack
Python — Pandas, NumPy, SciPy (`stats.pearsonr`), Matplotlib, Seaborn

## 🔄 Methodology (general approach)
- Merged and de-duplicated multiple related tables (home/away players, match events, tournaments, statistics) using `match_id` as the join key.
- Applied the **IQR method** to detect and filter outliers (e.g., unrealistic match durations).
- Used grouping/aggregation (`groupby`, `value_counts`, `crosstab`) to summarize player, country, and gender-level statistics.
- Used **Pearson correlation** to test the relationship between numerical variables (e.g., height vs. ranking).
- Visualized every answer with a purpose-built chart (histograms, bar charts, scatter plots).

## 📊 Key Findings

| # | Question | Answer |
|---|---|---|
| 1 | How many unique players are in the dataset? | **2,635** unique players (ATP + WTA) |
| 2 | What is the average player height? | **1.82 m** (182 cm); males average 1.84 m vs. females 1.73 m |
| 3 | Which player has the most wins? | **Popko**, with **30** wins |
| 4 | What is the longest recorded match? | **4 hours 20 minutes** (after outlier filtering with IQR) |
| 5 | How many sets are typically played? | **2 sets** on average (best-of-three format) |
| 6 | Which country has produced the most successful players? | **USA** |
| 7 | Average number of aces per match? | **7 aces** per match |
| 8 | Do double faults differ by gender? | Yes — male players average **~1.3% more** double faults per match than female players |
| 9 | Who won the most tournaments in a single month? | **Popko D.** — 18 tournaments in February |
| 10 | Is there a correlation between height and ranking? | **Extremely weak** linear relationship (Pearson correlation ≈ 0) |
| 13 | Left- vs. right-handed player distribution? | **88.4%** right-handed vs. **11.6%** left-handed |
| 14 | Most common tournament surface? | **Hardcourt (outdoor)** |
| 15 | How many distinct countries are represented? | **100 countries** |
| 16 | Highest win % against Top-10 ranked opponents (min. 5 matches)? | Led by players such as **Humbert** and **Świątek** |
| 17 | Average number of serve breaks per match? | **~14.2** breaks per match |

## 📁 Repository Contents
| File | Description |
|---|---|
| `final_TennisMatch_analyz.ipynb` | Main analysis notebook — all 15 questions, methodology, and visualizations |
| `parquet to csv.ipynb` | Data conversion notebook (Parquet → CSV) |
| `final_presentation.pdf` | Summary presentation of the project and findings |

## 👤 Author
**Fateme Toosi Moghadam**
[LinkedIn](https://www.linkedin.com/in/fateme-toosi-moghadam) | ftoosimoghadam@gmail.com
