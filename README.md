# Residential Property Price Index Forecasting Project
Utilized advanced machine learning techniques to develop a robust model forecasting residential property price indices (RPPI) in Istanbul, Turkey.

<p align="center"><img src="image/3_readme_rppi_definition_image.png" width="800"" /></p>

**Authors and Contact Information:** 
- [Asli Keser](https://github.com/aslikeser)
- [Linkedin](https://www.linkedin.com/in/asli-keser/)
- [aslikeser7@gmail.com](mailto:aslikeser7@gmail.com)

## Overview
In the last two years, housing prices in Turkey have skyrocketed, **quadrupling** in an unprecedented surge that has reshaped the real estate landscape.
The volatile nature of the Turkish real estate market demands accurate forecasting of housing prices.

<p align="center"><img src="image/1_readme_overview_image.png" width="800" /></p>

Also, in the last two years, the number of years spent to save a **30% down payment** for a **750 sq ft apartment** with the assumption that **the amount of net minimum wage saved every month** got as high as **13.3 years**. 

<p align="center"><img src="image/2_readme_overview_image.png" width="800" " /></p>

## Business Problem
This project aims to leverage predictive analytics techniques on historical housing data to develop a robust machine learning model, enabling stakeholders to
- anticipate future price trends,
- navigate market fluctuations,
- make informed decisions in the evolving landscape of the Turkish housing market.

The volatile nature of the Turkish real estate market demands an understanding of the market dynamics and accurate forecasting of housing prices.

## Data Collection

<p align="center"><img src="image/4_readme_data_collection_image.png" width="800" " /></p>

<ins>**Data Range and Frequency**</ins>   
**Data Frequency**: Monthly      
**Date Range**: January 2014 - August 2023   

<ins>**Data Sources**</ins>       
[Database of the Central Bank of the Republic of Turkey](https://evds2.tcmb.gov.tr/)    
[Google Trends](https://trends.google.com/trends/)  

<ins>**Data Dictionary**</ins>  
| Column Name | Description |
| :--- | :--- |
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
| **Inflation**|
| `Inflation_monthly_%` | Monthly inflation rate in Turkey |
| `Inflation_yearly_%` | Yearly inflation rate in Turkey |
| **Interest Rate**|
| `cb_key_interest_rate` | Central Bank of Turkey key interest rate |
| `avg_mortgage_interest_rate` | Average mortgage interest rate |
| **Minimum Wage**|
| `net_min_wage_TRY` | Net minimum wage in TRY |
| `gross_min_wage_TRY` | Gross minimum wage in TRY |
| **Exchange Rate**|
| `exchange_rate_usd-try` | Exchange rate of USD to TRY |
| `exchange_rate_rub-try` | Exchange rate of RUB to TRY |
| `exchange_rate_irr-try` | Exchange rate of IRR to TRY |
| `exchange_rate_iqd-try` | Exchange rate of IQD to TRY |
| **Foreign Investment** |
| `foreign_res_prop_sales_turkey` | Residential property sales to foreigners in Turkey |
| **Import & Export**|
| `export_1000usd` | Export amount in units in $1000 |
| `import_1000usd` | Import amount in units in $1000 |
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
| **Housing Price**|
| `istanbul_housing_unit_price_tl/m2` | Average unit price per square meter in TRY |
| **Residential Property Price Index (RPPI)**|
| `res_price_index_ist` | PPI for all residential buildings in Istanbul |  

<ins>**Data Range and Frequency**</ins>   
## Data Analysis
In conclusion of my comprehensive exploratory data analysis on real estate price fluctuations in Turkey, it is evident that <ins>the residential real estate market is highly sensitive to foreign investment</ins>. Notably, <ins>government policies concerning foreign investment</ins>, coupled with <ins>global economic and political trends</ins>, exert a significant influence on the fluctuations observed in the Turkish real estate market.

In October 2018, the Turkish government announced a substantial reduction in the threshold for gaining Turkish citizenship through investment, decreasing it from $1 million to $250,000. This policy shift positioned Turkey as an attractive destination for investment migration, particularly for individuals from politically unstable countries surrounding Turkey. However, the subsequent surge in foreign demand for real estate in Turkey had repercussions. As the demand increased, so did housing prices, rendering the market less accessible for Turkish citizens.

Based on data provided by the Central Bank of the Republic of Turkey, a substantial portion of foreign investments in real estate is concentrated in five key cities: Istanbul, Antalya, Izmir, Mugla, and Mersin. Over the past decade, three countries —Russia, Iran, and Iraq— have dominated these investments, accounting for as much as 56% of the total. The period following 2022 saw a notable increase in Russian interest in the Turkish real estate market, influenced in part by the Russia-Ukraine war.

During the initial six months following the commencement of the Russia-Ukraine war, residential property sales in the top five cities in Turkey experienced a significant surge. Notably, one in every six sales during this period was attributed to foreign buyers.

<p align="center"><img src="image/5_readme_data_analysis_image.png" width="800" " /></p>

For a more detailed exploration of these findings and the impact of government policies on foreign investment, please refer to the corresponding figures presented in my GitHub repository.


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







