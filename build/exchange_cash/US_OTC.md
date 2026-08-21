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
| Depository Receipt |           1816 | 10.29%       |
| ETF                |            709 | 4.02%        |
| ETN                |             17 | 0.1%         |
| Equity             |          14435 | 81.81%       |
| Preferred Stock    |            271 | 1.54%        |
| REIT               |             46 | 0.26%        |
| Right              |             17 | 0.1%         |
| Unit               |            126 | 0.71%        |
| Unknown            |             14 | 0.08%        |
| Warrant            |            192 | 1.09%        |
| Total              |          17644 | 100%         |


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


