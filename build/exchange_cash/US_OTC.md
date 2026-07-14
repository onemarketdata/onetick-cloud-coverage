# US OTC Equities (Trades only)

FINRA reported trades for OTC instruments

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20160104
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for US_OTC`
* `Field Enumerations for US_OTC`
* `Trading Hours for US_OTC`
* `Recent Holidays for US_OTC`



Includes the following coverage:

#### US_OTC -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |              1 | 0.01%        |
| Depository Receipt |           1801 | 10.21%       |
| ETF                |            703 | 3.99%        |
| ETN                |             17 | 0.1%         |
| Equity             |          14429 | 81.82%       |
| Preferred Stock    |            274 | 1.55%        |
| REIT               |             47 | 0.27%        |
| Right              |             20 | 0.11%        |
| Unit               |            128 | 0.73%        |
| Unknown            |             11 | 0.06%        |
| Warrant            |            204 | 1.16%        |
| Total              |          17635 | 100%         |


Consists of 3 Databases

* `US_OTC`  - Tick Data
* `US_OTC_BARS`  - 1 Minute Bars
* `US_OTC_DAILY`  - End of Day Metrics




## US_OTC

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## US_OTC_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## US_OTC_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


