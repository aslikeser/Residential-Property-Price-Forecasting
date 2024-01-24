# Residential Property Price Index Forecasting Project
Utilized advanced machine learning techniques to develop a robust model forecasting residential property price indices (RPPI) in Istanbul, Turkey.

<p align="center"><img src="image/3_readme_rppi_definition_image.png" width="70%" height="70%" /></p>

**Authors and Contact Information:** 
- [Asli Keser](https://github.com/aslikeser)
- [Linkedin](https://www.linkedin.com/in/asli-keser/)
- [aslikeser7@gmail.com](mailto:aslikeser7@gmail.com)

## Overview
In the last two years, housing prices in Turkey have skyrocketed, **quadrupling** in an unprecedented surge that has reshaped the real estate landscape.
The volatile nature of the Turkish real estate market demands accurate forecasting of housing prices.

<p align="center"><img src="image/1_readme_overview_image.png" width="70%" height="70%" /></p>

Also, in the last two years, the number of years spent to save a **30% down payment** for a **750 sq ft apartment** with the assumption that **the amount of net minimum wage saved every month** got as high as **13.3 years**. 

<p align="center"><img src="image/1_readme_overview_image.png" width="70%" height="70%" /></p>

## Business Problem
This project aims to leverage predictive analytics techniques on historical housing data to develop a robust machine learning model, enabling stakeholders to
- anticipate future price trends,
- navigate market fluctuations,
- make informed decisions in the evolving landscape of the Turkish housing market.

The volatile nature of the Turkish real estate market demands an understanding of the market dynamics and accurate forecasting of housing prices.

### What factors contribute to changes in housing prices?
- Supply and Demand Dynamics
- Interest Rates
- Foreign Investment
- Government Policies
- Inflation
- Speculation
- Global Economic Trends

**Location**: Istanbul, Turkey  
**Data Frequency**: Monthly  
**Date Range**: January 2014 - August 2023

# Data Dictionary

| Column Name | Description |
| --- | --- |
| **Supply** |
| `const_perm_res_1_dwelling_num_of_units_public` | The number of residential units with 1 dwelling in buildings that received construction permits and will be constructed by public construction companies |
| `const_perm_res_1_dwelling_num_of_units_coop` | The number of residential units with 1 dwelling in buildings that received construction permits and will be constructed by cooperations |
| `const_perm_res_1_dwelling_num_of_units_private` | The number of residential units with 1 dwelling in buildings that received construction permits and will be constructed by private construction companies |
| `const_perm_res_2+dwelling_num_of_units_public` | The number of residential units with 2+ dwellings in buildings that received construction permits and will be constructed by public construction companies |
| `const_perm_res_2+dwelling_num_of_units_coop` | The number of residential units with 2+ dwellings in buildings that received construction permits and will be constructed by cooperations |
| `const_perm_res_2+dwelling_num_of_units_private` | The number of residential units with 2+ dwellings in buildings that received construction permits and will be constructed by private construction companies |
| **Demand** |
| `mortgaged_first_sale_ist` | Mortgaged first-time sales in Istanbul |
| `mortgaged_second+_sale_ist` | Mortgaged second or more time sales in Istanbul |
| `not_mortgaged_first_sale_ist` | Cash first-time sales in Istanbul |
| `not_mortgaged_second+_sale_ist` | Cash second or more time sales in Istanbul |
| **Foreign Investment** |
| `foreign_res_prop_sales_turkey` | Residential property sales to foreigners in Turkey |
| **Exchange Rate**|
| `exchange_rate_usd-try` | Exchange rate of USD to TRY |
| `exchange_rate_rub-try` | Exchange rate of RUB to TRY |
| `exchange_rate_irr-try` | Exchange rate of IRR to TRY |
| `exchange_rate_iqd-try` | Exchange rate of IQD to TRY |
| **Minimum Wage**|
| `net_min_wage_TRY` | Net minimum wage in TRY |
| `gross_min_wage_TRY` | Gross minimum wage in TRY |
| **Interest Rate**|
| `cb_key_interest_rate` | Central Bank of Turkey key interest rate |
| `avg_mortgage_interest_rate` | Average mortgage interest rate |
| **Inflation**|
| `Inflation_monthly_%` | Monthly inflation rate in Turkey |
| `Inflation_yearly_%` | Yearly inflation rate in Turkey |
| **Import/Export**|
| `export_1000usd` | Export amount in units in $1000 |
| `import_1000usd` | Import amount in units in $1000 |
| **Housing Price**|
| `istanbul_housing_unit_price_tl/m2` | Average unit price per square meter in TRY |
| **Google Trends**|
| `inflation_google_trend_ist` | Relative search volume of word “inflation” in Istanbul, Turkey from Google Trends (0-100) |
| `usd_exc_rate_google_trend_ist` | Relative search volume of the phrase “dollar exchange rate” in Istanbul, Turkey from Google Trends (0-100) |
| `real_estate_in_Turkey__Russia_google_trends` | Relative search volume of the phrase “real estate in Turkey” in Russia from Google Trends (0-100) |
| `Turkish_citizenship__Russia__google_trends` | Relative search volume of the phrase “Turkish citizenship” in Russia from Google Trends (0-100) |
| `living_in_Turkey__Russia__google_trends` | Relative search volume of the phrase “living in Turkey” in Russia from Google Trends (0-100) |
| `buying_a_house_in_Turkey__Iran__google_trends` | Relative search volume of the phrase “buying a house in Turkey” in Iran from Google Trends (0-100) |
| `Turkish_citizenship__Iran__google_trends` | Relative search volume of the phrase “Turkish citizenship” in Iran from Google Trends (0-100) |
| `investmen_migration__Iran__google_trends` | Relative search volume of the phrase “investment migration” in Iran from Google Trends (0-100) |
| `living_in_Turkey__Iran__google_trends` | Relative search volume of the phrase “living in Turkey” in Iran from Google Trends (0-100) |
| `life_in_Turkey__Iraq__google_trends` | Relative search volume of the phrase “life in Turkey” in Iraq from Google Trends (0-100) |
| `Turkish_citizenship__Iraq__google_trends` | Relative search volume of the phrase “Turkish citizenship” in Iraq from Google Trends (0-100) |
| **Residential Property Price Index (RPPI)**|
| `res_price_index_ist` | PPI for all residential buildings in Istanbul |

### Data Sources:
[Database of the Central Bank of the Republic of Turkey](https://evds2.tcmb.gov.tr/)    
[Google Trends](https://trends.google.com/trends/)    






__Note:__ From “Eksi Sozluk” aka “Reddit of Turkey”, extract every entry relating to buying a house and apply sentiment analysis to reflect how Turkish people’s opinion of buying a house is affected by the volatility of the real estate market this will help the predictive model to take into account the speculation component of real estate market.

# Roadmap
1) Data Collection
2) Data Cleaning and Processing
3) Exploratory Data Analysis (EDA)
4) Model Selection
  - Linear Regression Model
  - Time Series Analysis
  - NLP
6) Model Training
7) Model Evaluation
  - Linear Regression Model -> R-squared & RMSE
8) Validation and Optimization







