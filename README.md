# Silver Tsunami Homes by State and County: Owner-Occupied Homes Headed by Seniors 65+ and 75+

Counts, shares and aggregate value of owner-occupied homes whose householder is 65+ or 75+, for every state (ACS 2024 1-year) and every county (ACS 2020-2024 5-year).

**Live page:** https://familyestateguide.com/estate-planning-data/silver-tsunami-homes-by-state/  
**Publisher:** Family Estate Guide (https://familyestateguide.com)  
**Version:** 1.0.0 (2026-10-02)  
**License:** CC BY 4.0 (data). See LICENSE.

> Not legal, tax, financial or medical advice. Figures are estimates with sampling error; legal rules change. Verify anything important with the original source or a qualified professional.

## Files

| File | Rows | Contents |
|---|---|---|
| `data/silver_tsunami_states_acs2024_1yr.csv` | 51 | 51 rows (50 states + DC), ACS 2024 1-year. |
| `data/silver_tsunami_us_acs2024_1yr.csv` | 1 | 1 row, United States, ACS 2024 1-year. |
| `data/silver_tsunami_counties_acs2020_2024_5yr.csv` | 3144 | 3,144 counties and county-equivalents (Puerto Rico excluded), ACS 2020-2024 5-year. No median or rank columns. |

Blank cells mean not available, not published or not applicable; they are never zero.

## Data dictionary

### `data/silver_tsunami_states_acs2024_1yr.csv`

| Column | Description |
|---|---|
| `name` | Geography name as published by the Census Bureau. |
| `state_fips` | Two-digit state FIPS code. |
| `occupied_homes` | Occupied housing units (B25007_001E). |
| `owner_homes_total` | Owner-occupied housing units (B25007_002E). |
| `owner_homes_total_moe` | 90% margin of error for owner_homes_total. |
| `owner_65_74` | Owner-occupied units, householder aged 65-74 (B25007_009E). |
| `owner_75_84` | Owner-occupied units, householder aged 75-84 (B25007_010E). |
| `owner_85plus` | Owner-occupied units, householder aged 85+ (B25007_011E). |
| `owner_65plus` | owner_65_74 + owner_75_84 + owner_85plus. |
| `owner_75plus` | owner_75_84 + owner_85plus. |
| `owner_65plus_moe` | Approximate 90% MOE of owner_65plus (root sum of squares of component MOEs). |
| `owner_75plus_moe` | Approximate 90% MOE of owner_75plus (root sum of squares). |
| `share_owner_homes_65plus_pct` | owner_65plus as % of owner_homes_total. |
| `share_owner_homes_75plus_pct` | owner_75plus as % of owner_homes_total. |
| `share_owner_homes_65plus_moe_pct` | Approximate 90% MOE of the 65+ share, percentage points (Census proportion formula). |
| `share_owner_homes_75plus_moe_pct` | Approximate 90% MOE of the 75+ share, percentage points. |
| `households_65plus` | Occupied units (owner + renter) with householder 65+ (B25007 009-011 + 019-021). |
| `homeownership_rate_65plus_pct` | owner_65plus as % of households_65plus. |
| `aggregate_value_all_owner_homes_usd` | Aggregate owner-reported value of all owner-occupied units, USD (B25079_001E). |
| `aggregate_value_65plus_usd` | Aggregate value of owner-occupied units with householder 65+, USD (B25079_005E). |
| `aggregate_value_65plus_moe_usd` | 90% MOE of aggregate_value_65plus_usd (B25079_005M). |
| `share_of_home_value_held_by_65plus_pct` | aggregate_value_65plus_usd as % of aggregate_value_all_owner_homes_usd. |
| `avg_value_per_65plus_owner_home_usd` | aggregate_value_65plus_usd / owner_65plus (mean, pulled up by expensive homes). |
| `median_value_65plus_householder_usd` | Median value, owner-occupied units with householder 65+, USD (S0103_C02_098E). |
| `median_value_65plus_householder_moe_usd` | 90% MOE of the 65+ median value (S0103_C02_098M). |
| `median_value_all_owner_homes_usd` | Median value, all owner-occupied units, USD (S0103_C01_098E). |
| `rank_owner_75plus_count` | Rank by owner_75plus, 1 = most homes. |
| `rank_share_75plus` | Rank by share_owner_homes_75plus_pct, 1 = highest share. |
| `rank_share_65plus` | Rank by share_owner_homes_65plus_pct, 1 = highest share. |

### `data/silver_tsunami_us_acs2024_1yr.csv`

| Column | Description |
|---|---|
| `name` | Geography name as published by the Census Bureau. |
| `us_fips` | Census API 'us' geography code (1). |
| `occupied_homes` | Occupied housing units (B25007_001E). |
| `owner_homes_total` | Owner-occupied housing units (B25007_002E). |
| `owner_homes_total_moe` | 90% margin of error for owner_homes_total. |
| `owner_65_74` | Owner-occupied units, householder aged 65-74 (B25007_009E). |
| `owner_75_84` | Owner-occupied units, householder aged 75-84 (B25007_010E). |
| `owner_85plus` | Owner-occupied units, householder aged 85+ (B25007_011E). |
| `owner_65plus` | owner_65_74 + owner_75_84 + owner_85plus. |
| `owner_75plus` | owner_75_84 + owner_85plus. |
| `owner_65plus_moe` | Approximate 90% MOE of owner_65plus (root sum of squares of component MOEs). |
| `owner_75plus_moe` | Approximate 90% MOE of owner_75plus (root sum of squares). |
| `share_owner_homes_65plus_pct` | owner_65plus as % of owner_homes_total. |
| `share_owner_homes_75plus_pct` | owner_75plus as % of owner_homes_total. |
| `share_owner_homes_65plus_moe_pct` | Approximate 90% MOE of the 65+ share, percentage points (Census proportion formula). |
| `share_owner_homes_75plus_moe_pct` | Approximate 90% MOE of the 75+ share, percentage points. |
| `households_65plus` | Occupied units (owner + renter) with householder 65+ (B25007 009-011 + 019-021). |
| `homeownership_rate_65plus_pct` | owner_65plus as % of households_65plus. |
| `aggregate_value_all_owner_homes_usd` | Aggregate owner-reported value of all owner-occupied units, USD (B25079_001E). |
| `aggregate_value_65plus_usd` | Aggregate value of owner-occupied units with householder 65+, USD (B25079_005E). |
| `aggregate_value_65plus_moe_usd` | 90% MOE of aggregate_value_65plus_usd (B25079_005M). |
| `share_of_home_value_held_by_65plus_pct` | aggregate_value_65plus_usd as % of aggregate_value_all_owner_homes_usd. |
| `avg_value_per_65plus_owner_home_usd` | aggregate_value_65plus_usd / owner_65plus (mean, pulled up by expensive homes). |
| `median_value_65plus_householder_usd` | Median value, owner-occupied units with householder 65+, USD (S0103_C02_098E). |
| `median_value_65plus_householder_moe_usd` | 90% MOE of the 65+ median value (S0103_C02_098M). |
| `median_value_all_owner_homes_usd` | Median value, all owner-occupied units, USD (S0103_C01_098E). |

### `data/silver_tsunami_counties_acs2020_2024_5yr.csv`

| Column | Description |
|---|---|
| `name` | Geography name as published by the Census Bureau. |
| `state_fips` | Two-digit state FIPS code. |
| `county_fips` | Three-digit county FIPS code (combine with state_fips for the 5-digit code). |
| `occupied_homes` | Occupied housing units (B25007_001E). |
| `owner_homes_total` | Owner-occupied housing units (B25007_002E). |
| `owner_homes_total_moe` | 90% margin of error for owner_homes_total. |
| `owner_65_74` | Owner-occupied units, householder aged 65-74 (B25007_009E). |
| `owner_75_84` | Owner-occupied units, householder aged 75-84 (B25007_010E). |
| `owner_85plus` | Owner-occupied units, householder aged 85+ (B25007_011E). |
| `owner_65plus` | owner_65_74 + owner_75_84 + owner_85plus. |
| `owner_75plus` | owner_75_84 + owner_85plus. |
| `owner_65plus_moe` | Approximate 90% MOE of owner_65plus (root sum of squares of component MOEs). |
| `owner_75plus_moe` | Approximate 90% MOE of owner_75plus (root sum of squares). |
| `share_owner_homes_65plus_pct` | owner_65plus as % of owner_homes_total. |
| `share_owner_homes_75plus_pct` | owner_75plus as % of owner_homes_total. |
| `share_owner_homes_65plus_moe_pct` | Approximate 90% MOE of the 65+ share, percentage points (Census proportion formula). |
| `share_owner_homes_75plus_moe_pct` | Approximate 90% MOE of the 75+ share, percentage points. |
| `households_65plus` | Occupied units (owner + renter) with householder 65+ (B25007 009-011 + 019-021). |
| `homeownership_rate_65plus_pct` | owner_65plus as % of households_65plus. |
| `aggregate_value_all_owner_homes_usd` | Aggregate owner-reported value of all owner-occupied units, USD (B25079_001E). |
| `aggregate_value_65plus_usd` | Aggregate value of owner-occupied units with householder 65+, USD (B25079_005E). |
| `aggregate_value_65plus_moe_usd` | 90% MOE of aggregate_value_65plus_usd (B25079_005M). |
| `share_of_home_value_held_by_65plus_pct` | aggregate_value_65plus_usd as % of aggregate_value_all_owner_homes_usd. |
| `avg_value_per_65plus_owner_home_usd` | aggregate_value_65plus_usd / owner_65plus (mean, pulled up by expensive homes). |

## Sources

- U.S. Census Bureau, American Community Survey (ACS) 2024 1-year, table(s) B25007 (tenure by age of householder), B25079 (aggregate value by age of householder), S0103 (population 65+), via the Census Data API (https://api.census.gov/data/2024/acs/). Public domain.
- U.S. Census Bureau, American Community Survey (ACS) 2020-2024 5-year (counties), table(s) B25007, B25079, via the Census Data API (https://api.census.gov/data/2024/acs/). Public domain.

## Methodology

- States and U.S. use ACS 2024 1-year; counties use ACS 2020-2024 5-year. The U.S. row comes from the API's us:1 geography, not a sum of states.
- Census annotation sentinels (e.g., -666666666) are set to blank, never zero. 471 small counties have no published aggregate value.

## Limitations

- 'Next 10 years' framing on the live page is editorial; the Census Bureau does not project home transfers.
- Householder is not necessarily the sole owner; value is owner-reported and gross of any mortgage; only occupied primary homes are counted.
- County 5-year estimates are not directly comparable with state 1-year estimates.
- Several state ranks overlap within margins of error (e.g., California vs. Florida 75+ counts).
- ACS 2025 1-year was delayed by the Census Bureau; refresh when released.

## Rights review and exclusions

Family Estate Guide publishes here only its own compiled data and U.S. government public-domain data (Census, BLS, CMS, DOL), plus third-party data that is under CC BY or a compatible open license, with attribution. Third-party copyrighted or non-commercial-licensed data is excluded.

- None. All columns derive from Census public-domain data.

## How to cite

Family Estate Guide (2026). *Silver Tsunami Homes by State and County: Owner-Occupied Homes Headed by Seniors 65+ and 75+* (Version 1.0.0) [Data set]. https://familyestateguide.com/estate-planning-data/silver-tsunami-homes-by-state/ . GitHub: https://github.com/jameyriley46-ux/familyestateguide-silver-tsunami-homes-by-state

A Zenodo DOI will be added here once version 1.0.0 is released and archived. Machine-readable citation: `CITATION.cff`.

Please link to the live page when you use the data.

## License

Data in this repository is licensed under the Creative Commons Attribution 4.0 International license (CC BY 4.0). Underlying U.S. government data is public domain; third-party CC BY data keeps its original attribution requirements (see Sources).
