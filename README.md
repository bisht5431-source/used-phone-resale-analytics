<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Poppins&size=28&duration=3000&pause=1000&color=534AB7&center=true&vCenter=true&width=650&lines=Used+Phone+Resale+Analytics;Power+BI+%2B+DAX+on+1M+Records;Built+by+Manish" alt="Typing SVG" />

<br/>

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-534AB7?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-1D9E75?style=for-the-badge)

*Turning 1 million used-phone listings into a clear story about what actually holds resale value.*

</div>

---

## 📌 About This Project

A **two-page Power BI report** analyzing **1,000,000 used phone listings** (2019–2025) to understand what drives resale value — brand, condition, age, repair history, warranty coverage, and seller type. The report is split into an **Overview** page (high-level KPIs and market trends) and an **Analysis** page (deeper diagnostic visuals — retention ratios, repair/warranty impact, and top-performing models).

---

## 🖼️ Dashboard Preview

### Overview Page
<img width="1379" height="726" alt="Screenshot 2026-07-15 112741" src="https://github.com/user-attachments/assets/250c09fb-f5ca-4f82-ad3f-10f45dc888a6" />


### Analysis Page
<img width="1378" height="731" alt="Screenshot 2026-07-15 112807" src="https://github.com/user-attachments/assets/665cb7ba-3230-4927-9178-30ef364c0119" />


---

## 🗂️ Report Pages

| Page | What It Shows |
|---|---|
| **Overview** | KPI cards, average resale price by brand, depreciation by condition, battery capacity by OS type, and resale price trend by age band |
| **Analysis** | Original vs resale price by brand, price retention ratio ranking, repair history impact, warranty band impact, seller type split, and top 5 models by resale value |

**Filters:** Model · Brand · City Tier — synced across both pages, with a one-click reset button.

---

## 🎯 Key KPIs

| Metric | Value |
|---|---|
| Total Listings | 1.0M |
| Average Resale Price | ₹22,598 |
| Average Original Price | ₹79,966 |
| Damaged Phones % | 21.43% |
| Average Market Demand Score | 70.02 |

---

## 💡 Key Insights

- **Apple retains value best** — highest price retention ratio (34%) of any brand, well ahead of Samsung and Google (~30%)
- **Condition drives depreciation predictably** — average depreciation climbs steadily from 66% (Excellent) to 80% (Poor)
- **Repair history hurts resale value** — never-repaired phones total ₹19.4bn in resale value vs ₹3.2bn for repaired ones
- **Warranty coverage adds real value** — phones with 12+ months of warranty remaining resell notably higher than those with none
- **Android dominates the market** (85.71% of listings) but **iOS commands a higher average resale price**
- **Top resale performers**: Vivo V27, Vivo X90, Realme Narzo 60, Realme GT, and Pixel 7 lead all individual models by total resale value

---

## 🧮 Sample DAX Measures

```dax
Price Retention Ratio = 
DIVIDE(
    AVERAGE(used_phone_price_prediction_1M[resale_price]),
    AVERAGE(used_phone_price_prediction_1M[original_price]),
    0
) * 100
```

```dax
Avg Depreciation by Condition = 
AVERAGE(used_phone_price_prediction_1M[Depreciation_Percent])
```

```dax
Damaged Phones % = 
DIVIDE(
    CALCULATE(COUNTROWS(used_phone_price_prediction_1M), used_phone_price_prediction_1M[Damage_Status] = "Damaged"),
    [Total Listings],
    0
) * 100
```

---

## 🛠️ Tools & Technologies

<div align="center">

![Power BI](https://img.shields.io/badge/Power%20BI%20Desktop-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

</div>

---

## 📊 Data Model

**used_phone_price_prediction_1M** (single fact table, 1M rows, 28 columns)

Key columns: `model, brand, os_type, original_price, resale_price, age_months, condition, city_tier, seller_type, repair_history, warranty_remaining_months, screen_cracked, body_damage, water_damage, battery_health, market_demand_score`

Key calculated columns: `Depreciation_Percent, Age_Band, Damage_Status, Warranty_Band, Repair_Status`

---

## 📂 Repository Structure

```
used-phone-resale-analytics/
│
├── assets/
│   ├── overview.png
│   └── analysis.png
├── data/
│   └── used_phone_price_prediction_1M.csv
├── Used_Phone_Analysis.pbix
└── README.md
```

---

## 🚀 How to Use

1. Clone this repository
   ```bash
   git clone https://github.com/bisht5431-source/used-phone-resale-analytics.git
   ```
2. Open `Used_Phone_Analysis.pbix` in **Power BI Desktop**
3. Use the Model, Brand, and City Tier filters at the top to slice the data
4. Toggle between **Overview** and **Analysis** using the in-report navigation buttons

---

<div align="center">

## 👋 About Me

<img src="https://readme-typing-svg.demolab.com?font=Poppins&size=20&duration=2500&pause=800&color=1D9E75&center=true&vCenter=true&width=500&lines=Data+Analyst+%7C+SQL+%2B+Power+BI+%2B+Python;6%2B+Years+Cross-Sector+Experience;IIT+Roorkee+Certified+in+Data+Analytics" alt="About Typing SVG" />

</div>

**Manish** — Data Analyst Intern @ Intellipaat Software Solutions, based in Delhi, India

I bring ~6 years of cross-sector experience (government, private, and technology) into data analytics, with an **Advanced Data Analytics certification from IIT Roorkee** and a B.Com from the University of Delhi. I specialize in turning large, messy datasets into dashboards that decision-makers can actually act on — this project analyzes 1 million rows end-to-end, from raw CSV to a fully interactive two-page Power BI report.

**🔧 Core Skills:** SQL (MySQL, PostgreSQL) · Power BI + DAX · Python (pandas) · Excel + Power Query · MIS Reporting

**📊 What I Build:** End-to-end analytics projects — from schema design and DAX measures to drillthrough-enabled dashboards — across domains like placements, healthcare, finance, e-commerce, and consumer electronics resale.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/dataanalyst-manish)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bisht5431-source)
[![Portfolio](https://img.shields.io/badge/Portfolio-534AB7?style=for-the-badge&logo=vercel&logoColor=white)](https://dashverse.lovable.app)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bisht5431@gmail.com)

</div>

<div align="center">

### 📈 GitHub Stats

<img src="https://github-readme-stats.vercel.app/api?username=bisht5431-source&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" height="165"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=bisht5431-source&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="165"/>

</div>

---

<div align="center">

⭐ **If this project helped you understand Power BI + DAX on large datasets, consider giving it a star!**

<img src="https://komarev.com/ghpvc/?username=bisht5431-source&style=for-the-badge&color=534AB7" alt="Profile Views" />

</div>
