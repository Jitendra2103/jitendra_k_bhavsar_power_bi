# Assignment 6 – Electric Vehicle Population Data Analysis (Power BI)

## 📌 Project Overview
This repository contains the Power BI report (`.pbix`) for **Assignment 6**, analyzing the **Electric Vehicle Population Dataset**. The dashboard tracks EV adoption growth, electric range efficiency, brand market share, Clean Alternative Fuel Vehicle (CAFV) eligibility, and geographic distribution.

---

## 🧹 Data Cleaning & Feature Engineering
The following data preparation steps were implemented in Power BI:
* **Standardized Vehicle Types:** Renamed `Battery Electric Vehicle (BEV)` to `Battery Electric Vehicle` and `Plug-in Hybrid Electric Vehicle (PHEV)` to `Hybrid Electric Vehicle`.
* **Blank Location Filtering:** Excluded all records where the `Vehicle Location` column was blank to maintain data integrity across geospatial visuals.
* **Electric Range Binning (`Electric Range Bin`):** Categorized electric range values into three tiers using DAX `SWITCH` logic:
  * **Low:** `0 – 100` miles
  * **Medium:** `101 – 200` miles
  * **High:** `> 200` miles
* **Coordinate Extraction (`Latitude_location` & `Longitude_location`):** Parsed the `POINT (val1 val2)` strings from `Vehicle Location` into two separate numeric columns (`Latitude_location` and `Longitude_location`).

---

## 📊 Key Performance Indicators (KPIs)
* **Total Vehicles:** Overall count of registered EVs (BEVs and PHEVs combined).
* **Average Electric Range:** Mean electric range across the dataset to measure battery efficiency improvements.
* **Total BEV Vehicles & % of Total:** Count and share of Battery Electric Vehicles.
* **Total PHEV Vehicles & % of Total:** Count and share of Hybrid Electric Vehicles.

---

## 📈 Dashboard Visualizations & Navigation
1. **Total Vehicles by Model Year (2011 Onwards):** Area/line trend chart tracking EV adoption growth from 2011 onward.
2. **Total Vehicles by State:** Geographic map illustrating EV concentration across states.
3. **Top 10 Total Vehicles by Make:** Ranked bar chart highlighting top EV manufacturers by market share.
4. **Total Vehicles by CAFV Eligibility:** Donut/proportion chart showing Clean Alternative Fuel Vehicle incentive eligibility.
5. **Top 10 Total Vehicles by Model:** Interactive visual with dynamic Top-N selection showcasing the most popular EV models.
6. **Multi-Page Navigation:** Includes **2 Navigation Buttons** on the main dashboard leading to secondary analytical views, paired with a **Back Button** on secondary screens to return seamlessly to the main dashboard.

---

## 🚀 How to View This Report
1. Download the `.pbix` file from this repository.
2. Open the file in **Microsoft Power BI Desktop**.
3. Use the slicers, dynamic Top-N controls, and page navigation buttons to explore the report.
