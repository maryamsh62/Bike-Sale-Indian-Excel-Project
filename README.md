# India Motorbike Resale Value Dashboard (Excel)

This project explores the resale market for motorcycles in India using an interactive Excel dashboard.  
The dataset from [Kaggle](https://www.kaggle.com/datasets/ak0212/indian-bike-sales-dataset) contains **10,000** synthetic but realistic records of bike sales/resales across Indian states, covering major brands such as **Honda, Royal Enfield, TVS, Yamaha, Hero, Bajaj, KTM, and Kawasaki**.

The Excel dashboard helps answer questions like:

- How do **resale prices** vary by **brand, state, and city tier**?
- Do **engine capacity**, **fuel type**, or **daily usage** affect resale value?
- How much value does a bike **lose from original price to resale price** (price gap)?
- How do **owner type** and **insurance status** impact resale prices?

---

## Dashboard Preview

![India Motorbike Resale Value Dashboard](India%20MotorBike%20Resale%20Value%20Dashboard.png)
The dashboard is fully interactive, using **PivotTables, PivotCharts, and Slicers**.

---

## Dataset Overview

File: `Indian Bike Sales Project.xlsx`, `Indian Bike Sales Dataset.xlsx`  
Sheet: `Indian_Bike_Sales Table`  

- **Rows:** 10,000 records  
- **Columns:** 18 features 

  This dataset and dashboard help analyze **market and resale trends** across Indian motorcycle brands, states, and city tiers.
  They reveal **consumer behavior and geographic patterns**, including how usage, owner type, fuel type, and insurance affect  pricing.
  The `Price Gap` metric supports **depreciation studies**, showing how quickly different brands and engine groups lose value.

### Core Columns

- `State` – Random Indian states represented in the dataset  
- `Avg Daily Distance(Km)` – Average daily distance traveled (between ~5–80 km)  
- `Brand` – One of the top 8 brands (Honda, Royal Enfield, TVS, Yamaha, Hero, Bajaj, KTM, Kawasaki)  
- `Model` – Random model names within each brand  
- `Price (INR)` – Original bike price (based on brand & model)  
- `Year of Manufacture` – Year bike was manufactured (2015–2024)  
- `Engine Capacity (cc)` – Engine displacement in cubic centimeters (100cc–1000cc)  
- `Fuel Type` – Petrol, Electric, or Hybrid  
- `Mileage (km/l)` – Fuel efficiency (varies by brand and engine size)  
- `Owner Type` – First, Second, or Third owner  
- `Registration Year` – Registration year (related to year of manufacture)  
- `Insurance Status` – Active, Expired, or Not Available  
- `Seller Type` – Dealer or Individual  
- `Resale Price (INR)` – Resale price computed using a depreciation formula  
- `City Tier` – Metro, Tier 1, Tier 2, or Tier 3 city

### Calculated columns

To enhance analysis and filtering, several derived fields were created:

- `Avg Daily Distance levels(Km):`

  - **High Usage** (>=41 Km)  
  - **Moderate Usage** (>=21 Km)  
  - **Lower Usage** (<21 Km)  
  These buckets group bikes by how heavily they are used, based on Avg Daily Distance(Km).
  

- `Engin Capacity Groups:`

  Engine capacities grouped into **four** intuitive ranges to simplify comparisons:
  
  **0-150 cc,  151-300 cc,  301-500 cc,  501-1000 cc**  
   

- `Price Gap`  
  **Price Gap = Price (INR) - Resale Price (INR)**
 
  This measures how much value the bike has lost from first sale to resale, and is used to study depreciation patterns by brand, owner type, and other attributes.


## Dashboard Components
The main dashboard brings together multiple PivotTables and charts:

- `Slicer Panel (Top Row)`

  Global filters that control all charts:

   **State, Brand, City Tier, Fuel Type, Owner Type, Seller Type, Insurance Status, Avg Daily Distance levels(Km), Engin Capacity Groups**


- `Avg Resale Price per State`

  Column chart displaying average resale price by Indian state,helping highlight states with relatively higher or lower resale values.


- `Avg Resale Price by Brand and City Tier`

  Clustered column chart comparing brands across city tiers, showing how resale performance differs between Metro, Tier 1, Tier 2, and Tier 3 cities.


- `Count of Bikes by Brand`

  Horizontal bar chart showing bike counts by brand, illustrating their relative representation and market share in the dataset.


- `Avg Resale Price by Year of Manufacture`

  Line chart tracking average resale price by manufacturing year (2015–2024), helping visualize how age and market trends affect resale value over time.
  
  
- `Avg Gap Price by Brand and Owner Type`

  Line chart based on the Price Gap metric, comparing depreciation across brands and owner types (First, Second, Third owner).


## Tools & Techniques

- Microsoft Excel
- Structured table for raw data (Bike_Sales_Indian Table)
- Conditional formulas for engineered columns
- PivotTables for aggregation and summarization
- PivotCharts for visualizations
- Slicers for interactive, multi-dimensional filtering
- Custom formatting, colors, and layout for a dashboard-style presentation



## Key Results & Insights

The dashboard reveals several interesting patterns in the synthetic Indian motorbike resale dataset:

1. **Resale value varies noticeably by state**  
   - Some states (e.g., Gujarat and Uttar Pradesh) show **higher-than-average resale prices**, suggesting stronger demand or better perceived condition of bikes in those markets.  
   - Others (such as Maharashtra and West Bengal) tend to sit **below the overall average**, indicating relatively weaker resale performance.

2. **Brand and City Tier have a strong combined impact on resale price**  
   - Premium or enthusiast brands (e.g., Royal Enfield, KTM, Kawasaki) generally command **higher resale values** across most city tiers.  
   - For many brands, **Tier 2 and Tier 3 cities often show slightly higher resale prices** than large Metro markets, hinting at lower depreciation or stronger demand in smaller cities within this dataset.

3. **Brand popularity vs. resale value**  
   - Brands like **Kawasaki, Yamaha, KTM, and Royal Enfield** have the **highest counts of bikes** in the dataset, reflecting strong representation and market presence.  
   - However, **high volume does not always equal the highest resale price**, which makes brand-wise comparison of price and price gap particularly insightful.

4. **Effect of manufacturing year on resale price**  
   - Newer model years (e.g., 2022–2024) expectedly show **higher average resale prices**, while older bikes from 2015–2017 trade at lower values.  
   - The trend line across 2015–2024 highlights how **age-related depreciation** combines with any changes in market pricing over time.
   
   
 ## Conclusion

This project showcases how Excel can be used as a powerful analytical and visualization tool for exploring a multi-dimensional dataset.  
Using a synthetic Indian motorbike resale dataset, the dashboard brings together **brands, states, city tiers, engine capacity, usage levels, ownership history, and insurance status** into one interactive view.

While the data is not real-market data, the patterns are intentionally designed to mimic plausible resale behavior.  
The result is a portfolio-ready project that demonstrates skills in:

- Data cleaning and feature engineering (`Price Gap`, usage and engine groups)
- Building PivotTables and PivotCharts
- Designing an interactive dashboard with slicers and filters
- Communicating insights about depreciation and value retention  


### How to Use This Project

- Clone or download the repository.
- Open Indian Bike Sales Project.xlsx in Excel (desktop recommended).
- Go to the Dashboard sheet. 
- Use the slicers at the top to explore the data

### Notes

- The dataset is synthetic and designed for learning and portfolio purposes.
- All patterns and insights reflect the data-generation logic rather than actual market data.




```python

```
