# Hong Kong Stock Exchange

The Hong Kong Stock Exchange (HKEX) offers trading in equities, bonds, ETFs, and derivatives issued by Hong Kong and international companies.

* Country: Hong Kong SAR China [HK]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Hong_Kong
* Start Date: 20080513
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for HKSE`
* `Field Enumerations for HKSE`
* `Trading Hours for HKSE`
* `Recent Holidays for HKSE`



Includes the following coverage:

#### HKSE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |           1386 | 6.08%        |
| Depository Receipt |              1 | 0.0%         |
| ETF                |            412 | 1.81%        |
| Equity             |           2802 | 12.3%        |
| Preferred Stock    |              1 | 0.0%         |
| REIT               |             11 | 0.05%        |
| Right              |             12 | 0.05%        |
| Statistics         |              2 | 0.01%        |
| Unknown            |             17 | 0.07%        |
| Warrant            |          18139 | 79.62%       |
| Total              |          22783 | 100%         |


Consists of 2 Databases

* `HKSE`  - Tick Data
* `HKSE_BARS`  - 1 Minute Bars




## HKSE

Database includes the following tick types:

* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## HKSE_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


