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
<img width="1189" height="659" alt="image" src="https://github.com/user-attachments/assets/a807e109-12a3-4019-87d2-6353c9662bb9" />


### Map Page
<img width="1219" height="650" alt="image" src="https://github.com/user-attachments/assets/b143d00a-e395-4ade-9461-abfc288894b5" />


### Simulator
<img width="1229" height="687" alt="image" src="https://github.com/user-attachments/assets/de97b2f0-db33-4d67-a683-ee395f931da8" />


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

## 🛠️ Tech Stack
- **Power BI** (DAX, Power Query, What-if Parameters)
- **Python/SQL** (optional for preprocessing, if you used it)
- **GitHub** for version control and sharing
