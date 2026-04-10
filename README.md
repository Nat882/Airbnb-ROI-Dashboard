# Airbnb Investment ROI Dashboard

A Power BI dashboard that models short-let investment returns across all 33 London boroughs, combining Land Registry property sales data with live Airbnb listings to surface net yield, NOI, and payback periods — with a what-if simulator for stress-testing assumptions.

---

## The problem

Property investors entering the London short-let market lack a practical way to compare net returns by borough against actual purchase prices. Headline gross yield figures ignore management fees, cleaning costs, and realistic occupancy — leaving investors with an incomplete picture. This dashboard bridges that gap.

---

## Dashboard pages

**Overview** — KPI cards for net yield %, gross yield %, and payback period, alongside a borough-level yield comparison and a time-series of median purchase prices and transaction volume.

**Map** — Azure Maps visual plotting net yield % and NOI across London by borough, with slicers for year, area, month, room type, and property type.

**Simulator** — Adjustable what-if parameters (management fee %, avg stay length, cleaning cost per stay, occupancy adjustment, platform fee %) that dynamically recalculate all ROI metrics. Includes a borough comparison table and top 5 NOI ranking.

---

## Key findings

Analysis across 33 London boroughs reveals several non-obvious conclusions:

- **Nightly rate drives returns more than occupancy** — correlation between avg nightly price and NOI is r=0.94, stronger than the occupancy–NOI relationship. A £100 difference in nightly rate outweighs a 10pp occupancy advantage in almost every borough.

- **High purchase prices don't kill yield** — purchase price and net yield are positively correlated (r=0.89). Westminster (£2.76M avg) still achieves 9.54% net yield; Kensington & Chelsea (£2.24M) returns 9.32%. Expensive boroughs command nightly rates that more than compensate for the higher entry cost.

- **The sweet spot is inner-south London** — Hackney (5.08%), Lambeth (4.91%), Southwark (4.86%), and Merton (4.79%) all exceed 4% net yield at under £800k entry price, with payback periods under 40 years — the best risk-adjusted returns in the dataset.

- **City of London is a yield trap** — a 6.53% gross yield looks attractive, but occupancy collapses to 31.8% (the lowest of any central borough), dragging net yield below Camden and pushing payback to 82 years.

- **Outer East London underperforms despite cheap entry** — Barking & Dagenham (£374k avg price) and Havering (£467k) yield only 1.9–2.05% net. Low nightly rates (£98–£114) and poor occupancy (27–29%) make the low entry price a false economy.

- **Cost drag is highest in premium boroughs** — Westminster and Kensington & Chelsea both carry a ~2.8pp gross-to-net spread, meaning fees and operating costs consume roughly a quarter of gross income.

- **January is the best time to buy** — median purchase prices in January (£268,100) sit 8.2% below the August peak (£290,000), with transaction volume also at its lowest (55k vs 74k in August).

---

## ROI metrics

| Metric | Definition |
|---|---|
| Gross yield % | (Avg nightly price × 365 × occupancy) / purchase price |
| Net yield % | NOI / purchase price |
| NOI | Gross revenue − management fee − cleaning costs − platform fee |
| Payback (years) | Purchase price / annual NOI |

Default simulator assumptions: 7-night avg stay, 10% management fee, 3% platform fee, occupancy from InsideAirbnb adjusted figures.

---

## Data sources

| Dataset | Source |
|---|---|
| Property sales (2020–2024) | [UK Land Registry Price Paid Data](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads) |
| Postcode → borough mapping | [ONS Postcode Directory (ONSPD)](https://geoportal.statistics.gov.uk/) |
| Airbnb listings and occupancy | [InsideAirbnb London](http://insideairbnb.com/get-the-data.html) |

---

## Tech stack

- **Power BI Desktop** — DAX measures, Power Query, what-if parameters, Azure Maps
- **DAX** — NOI, Net Yield %, Gross Yield %, Payback, dynamic scenario calculations
- **Power Query (M)** — postcode cleaning, ONSPD borough lookup join, PPD date filtering
- **GitHub + Git LFS** — version control for the .pbix file

---

## How to use

1. Clone this repo
2. Open `airbnb_roi_project.pbix` in Power BI Desktop (free)
3. If visuals show errors, go to Home → Transform Data → Data Source Settings and re-point to the source CSVs
4. Use the Simulator page slicers to adjust assumptions and observe the impact on yield and payback across boroughs

---

## Project structure

```
Airbnb-ROI-Dashboard/
├── airbnb_roi_project.pbix   # Main Power BI file
└── README.md
```

---

## About

Built as a portfolio project to demonstrate end-to-end data analytics — from raw government and open-source datasets through to an investor-facing decision tool. The focus was on business relevance: every metric exists to answer a question a real investor would ask before committing capital.
