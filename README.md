# Video Game Sales Analysis (1977–2018)

**What sells, and where?** An end-to-end analysis of 64,000+ video game sales records: data cleaning in Python, analysis of four business questions, and an interactive Tableau dashboard.

![Dashboard](Video%20Game%20Sales%20Project/dashboard.png)

🔗 **[View the interactive dashboard on Tableau Public](https://public.tableau.com/views/VideoGameSalesAnalysis1977-2018/VideoGameSalesDashboard)**

---

## Business questions
1. Which titles sold the most worldwide?
2. Which year had the highest sales? Is the industry growing?
3. Do any consoles specialize in a particular genre?
4. Which titles are popular in one region but flop in another?

## Key findings
- **GTA V is the best-selling title** (64.3M copies across 4 consoles). 7 of the top 10 are *Call of Duty* games.
- **Physical sales peaked in 2008 (538M copies)**, then declined as buying shifted to digital downloads, which this data doesn't track.
- **Consoles have genre identities:** Xbox One and PS4 lean on shooters, PC on simulation (7× the market average), and Nintendo handhelds on casual and platform games.
- **Japan is a different market:** RPGs are 18.5% of Japanese sales vs about 5% in the West, while shooters barely sell there.

## Data cleaning highlights
The raw data needed careful checking before analysis. Every decision is documented in the notebook with the evidence behind it:
- Removed 1,602 franchise summary rows ("Series" / "All" consoles) and titles with no sales data
- Cut the timeline at 2018 (2019–2020 had only ~30 games each, despite the "1971–2024" label)
- Found 176 partially tracked titles, e.g. *"(US sales)"* in the title, and excluded them from regional comparisons
- Identified that most Nintendo first-party hits (*Wii Sports*, *Mario Kart Wii*) have **no sales data**, and documented how this biases the results

**64,016 raw rows → 18,766 clean rows**

## Files
| File | Description |
|---|---|
| `video_game_sales_analysis.ipynb` | Full analysis: cleaning, Q1–Q4, conclusions |
| `vgchartz-2024.csv` | Raw data |
| `vg_data_dictionary.csv` | Column descriptions |
| `vg_sales_clean.csv` | Cleaned dataset used in Tableau |
| `vg_sales_by_region.csv` | Regional sales in long format for Tableau |

## Tools
Python (pandas, matplotlib, NumPy) · Jupyter Notebook · Tableau Public

## Data source
[VGChartz](https://www.vgchartz.com/) via [Maven Analytics Data Playground](https://mavenanalytics.io/data-playground) (license: ODC-BY)

## Limitations
- Physical sales only, so recent years are under-counted
- Only ~26% of Nintendo titles have sales figures
- Some games are filed under different regional names
