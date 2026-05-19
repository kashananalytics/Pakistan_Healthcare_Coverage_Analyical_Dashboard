<img width="1080" height="615" alt="WhatsApp Image 2026-05-17 at 10 15 21 PM" src="https://github.com/user-attachments/assets/62cc1d1a-bc06-4c4f-855f-c817d3a99c7d" />
Pakistan Healthcare Coverage Analytical Dashboard | Power BI 📊
<br>

Pakistan_Healthcare_Coverage_Analyical_Dashboard
Turned a raw Excel file into a full Healthcare Analytics Dashboard mapping Pakistan's 9K Hospitals, 17K Doctors, and Coverage gaps across 126 cities.
# 🏥 Pakistan Healthcare Coverage Analytical Dashboard

> An interactive Power BI dashboard analyzing hospital infrastructure across Pakistan — built from raw Excel data, cleaned with Power Query, and visualized with DAX-powered KPIs, maps, and charts.

---

## 📸 Dashboard Preview

![Dashboard Preview](dashboard.png)


---

## 📌 Project Summary

This project transforms a multi-sheet Excel dataset into a fully interactive **Power BI dashboard** that gives a clear picture of Pakistan's healthcare coverage — broken down by city, area, doctor count, and hospital density.

**Dataset size:** 8,652 hospitals · 126 cities · 2,000+ unique areas

---

## 📂 Dataset Overview

| Sheet | Records | Key Columns |
|---|---|---|
| Hospital Details | 8,652 | Name, City, Area, Address, Doctors, Contact |
| Hospital by Area | 2,190 | City, Area, Count, Density |
| Hospital by City | 126 | City, Total Hospitals |
| Top 4 Cities | 4 | City, Rank, Count |

---

## 🔢 KPI Cards (What the Dashboard Shows)

| KPI | Value |
|---|---|
| 🏥 Total Hospitals | 9K |
| 👨‍⚕️ Total Doctors | 17K |
| 🌆 Total Cities Covered | 126 |
| 🗺️ Total Areas Covered | 2K |
| 📊 Hospital Density | 6.56 |
| 🩺 Average Doctors per Hospital | 2.00 |
| 🏆 Top City (Lahore) | 2K+ |
| 📍 Average Hospitals per City | 68.00 |

---

## 📊 Visuals Built

✅ 8 KPI cards — Total Hospitals (9K), Total Doctors (17K), Cities Covered (126), Area Covered (2K), Top City (2K), Hospital Density (6.56), Average Doctor (2.00), Average City (68.00)

<br>

✅ City search bar — type any city name and every single visual updates instantly

<br>

✅ City filter tabs — one-click switching between Multan, Islamabad, Karachi, Lahore and Rawalpindi

<br>


✅ Bar chart — top 5 cities ranked by hospital count

<br>


✅ Donut chart — top 5 area wise distribution across Zarnar Shah, Zia Shah, Zikariya, Zikriya Town and Zilla Bha

<br>

✅ Interactive Bing Map — hospital pins plotted across Multan, Burewala, Muzaffargarh, Dunyapur, Lodhran and Jalalpur Pirwala

<br>

✅ Treemap — locality level breakdown showing Attock Cantt, Ghanta Ghar, Chak No 435 EB, Goat Chowk, Sargodha, Gull Bagh Colony, Township Sector C1, Faisalabad, Mardan and Lahore

---

## 🧮 Key DAX Measures

```dax
-- Total hospitals
Total Hospitals = COUNTROWS('Hospital Details')

-- Average doctors per hospital (excluding blanks)
Avg Doctors = AVERAGEX(FILTER('Hospital Details', 'Hospital Details'[DOCTORS] <> "-"), VALUE('Hospital Details'[DOCTORS]))

-- Hospital density per area
Hospital Density = DIVIDE([Total Hospitals], DISTINCTCOUNT('Hospital Details'[AREA]))

-- Average hospitals per city
Avg City = DIVIDE([Total Hospitals], DISTINCTCOUNT('Hospital Details'[CITY]))
```

---

## 🛠️ Tools Used

- **Microsoft Excel** — raw data source
- **Power Query** — data cleaning & transformation
- **Power BI Desktop** — dashboard design & layout
- **DAX** — custom KPI measures & calculations
- **Bing Maps** — geographic hospital location mapping

---

## 💡 Key Insights

- 🏙️ **Lahore alone** accounts for the largest hospital share nationally
- 📉 Only **2.00 average doctors** per hospital — a critical understaffing signal
- 🗺️ Despite 126 cities, coverage is **heavily urban-concentrated**
- 🔍 The treemap reveals **micro-locality gaps** invisible in city-level views

---

## 🚀 How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Use the city filter tabs at the top to explore each city
4. Click any bar, donut segment, or treemap block to cross-filter all visuals

---

*Built as a portfolio project. Feel free to fork, adapt, or use the DAX measures for your own healthcare or public-sector dashboards.*
<br>
## Author
Kashan Ahmed  
BS Statistics Graduate | Power BI & Data Analytics.
