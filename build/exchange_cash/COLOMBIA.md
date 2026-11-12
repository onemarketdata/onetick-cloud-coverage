# Colombia Stock Exchange

Trades, quotes and bars from the Colombia Stock Exchange (Bolsa de Valores de Colombia, BVC), with history from June 2016, covering Colombian equities and related products. Index data includes the MSCI COLCAP, Colombia’s main equity benchmark. BVC is now part of the nuam regional exchange group with the Santiago and Lima exchanges.

* Country: Colombia [CO]
* Mkt Hours: 08:00-17:00
* Time Zone: America/Bogota
* Start Date: 20160627
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: MSCI COLCAP [COLOMBIA::ICAP]



Details are provided below

* `Table Schemas for COLOMBIA`
* `Field Enumerations for COLOMBIA`
* `Trading Hours for COLOMBIA`
* `Recent Holidays for COLOMBIA`



Includes the following coverage:

#### COLOMBIA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |            428 | 63.98%       |
| ETF             |             88 | 13.15%       |
| Equity          |            138 | 20.63%       |
| Index           |             10 | 1.49%        |
| Unknown         |              5 | 0.75%        |
| Total           |            669 | 100%         |


Consists of 3 Databases

* `COLOMBIA`  - Tick Data
* `COLOMBIA_BARS`  - 1 Minute Bars
* `COLOMBIA_DAILY`  - End of Day Metrics




## COLOMBIA

Database includes the following tick types:

* IDX - Index values
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## COLOMBIA_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## COLOMBIA_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


