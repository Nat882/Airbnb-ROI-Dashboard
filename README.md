# Airbnb Investment ROI Dashboard 

## Overview
This project analyses **London property sales (Land Registry PPD)** and **Airbnb listings (InsideAirbnb)** to model **investment ROI**.  
The dashboard helps property investors assess **Net Yield %, Gross Yield %, Payback (years)**, and test scenarios with adjustable assumptions (cleaning cost, stay length, management fee %).

Built in **Power BI** using:
- DAX Measures (NOI, Net Yield %, Payback)
- Postcode mapping (ONSPD → Borough/Area)
- What-if parameters for ROI simulation
- Interactive slicers (Year, Area, Property Type, Room Type)

---

## Features
- **Overview Page:** KPIs + trends (median purchase price, transactions, yield by borough).
- **Map Page:** Visualises Net Yield % and NOI across London using Airbnb geodata.
- **Simulator Page:** Adjust assumptions (stay length, cleaning, mgmt fees) to test ROI scenarios.

---

## Screenshots
### Overview Page
<img width="1207" height="661" alt="image" src="https://github.com/user-attachments/assets/6a4bb07a-6db8-4446-afa9-695911cca8d1" />



### Map Page
<img width="1210" height="666" alt="image" src="https://github.com/user-attachments/assets/dedb8a00-2221-43f3-bea8-9dc5bf910c0a" />



### Simulator
<img width="1208" height="644" alt="image" src="https://github.com/user-attachments/assets/bc883722-ae7e-402b-a7b0-f51d01ce5892" />


---

## Data Sources
- [UK Land Registry Price Paid Data](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads)
- [ONS Postcode Directory (ONSPD)](https://geoportal.statistics.gov.uk/)
- [InsideAirbnb London Listings](http://insideairbnb.com/get-the-data.html)

---

## How to Use
1. Clone/download this repo. 
2. Open `Airbnb_ROI_Dashboard.pbix` in **Power BI Desktop**.
3. Refresh data (if local CSVs are connected).
4. Explore the pages:
   - Overview
   - Map
   - Simulator

---

## Insights
- Central London boroughs Westminster, Kensington & Chelsea have the **highest purchase prices** but still yield solid ROI due to high occupancy.
- Payback periods across London average ~18 years, but vary significantly by borough.
- Scenario testing shows how cleaning costs and management fees can reduce ROI by **1–2% Net Yield**.

---

## Tech Stack
- **Power BI** (DAX, Power Query, What-if Parameters)
- **Python/SQL** (optional for preprocessing, if you used it)
- **GitHub** for version control and sharing
