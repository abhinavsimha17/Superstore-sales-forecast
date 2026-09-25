# Sales Forecasting in Excel: Superstore 2019

Forecasting a retailer's monthly sales for 2019 using **only Excel formulas**. The model is tested on past data to prove it works, and it includes a what-if input for planning.

![Dashboard](dashboard.png)

## Dataset

[Superstore Sales dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) from Kaggle: 9,994 orders from a US retailer, Jan 2015 – Dec 2018, across Furniture, Office Supplies and Technology.

## Key results

| | |
|---|---|
| 2018 sales | $733K (+20% vs 2017) |
| **2019 forecast** | **$847K (+16%)** |
| Busiest month | November (85% above an average month) |
| Quietest months | January and February |
| Model error | 20% per month, beating the simpler methods |

## Key insights

1. **Growth continues.** Sales are forecast to grow 16% in 2019, which would be a third straight year of growth.
2. **Sales are very seasonal.** September, November and December bring in over 40% of the year's revenue, so stock and staff should be planned for Q4.
3. **January and February are slow.** They're a good window for promotions or maintenance.
4. **Technology stays the largest category** at a forecast $317K for 2019.

## How the forecast works

1. **Monthly sales:** add up orders by month with `SUMIFS`.
2. **Seasonality:** work out how each month compares with an average month (the seasonal index).
3. **Trend:** remove the seasonality and fit a straight-line trend with `TREND`.
4. **Forecast:** trend × seasonal index for each month of 2019.

## Proving it works (backtest)

I built three methods using only 2015–2017 data and checked them against what actually happened in 2018:

| Method | Avg monthly error |
|---|---|
| **Seasonal × trend** | **19.9%** (chosen) |
| Same month last year | 24.5% |
| Straight-line trend | 44.4% |

## What-if scenario

The yellow cell on the Dashboard lets you add a planned uplift, such as +5% for a new campaign. Every forecast number and chart updates automatically.

## Workbook tabs

| Tab | What it contains |
|---|---|
| Dashboard | KPIs, charts, insights and the scenario input |
| Monthly Forecast | The forecasting model |
| Backtest | Accuracy check on 2018 |
| Category | 2019 outlook by category |
| Data | The 9,994 raw orders |

## Excel skills used

`SUMIFS` · `AVERAGEIFS` · `TREND` · `FORECAST` · `INDEX/MATCH` · scenario input · line and bar charts · dashboard design
