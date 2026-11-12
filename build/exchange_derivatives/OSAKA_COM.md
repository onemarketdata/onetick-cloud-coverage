# Osaka Exchange - Commodity Derivatives (formerly TOCOM)

Futures, options and spreads with Trades, Quotes and bars from Osaka Exchange’s commodity derivatives market (formerly the Tokyo Commodity Exchange, TOCOM), with history from November 2009. Key contracts include gold, platinum and silver futures, rubber and other commodity contracts that moved from TOCOM to Osaka Exchange in 2020.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20091110
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for OSAKA_COM`
* `Field Enumerations for OSAKA_COM`
* `Trading Hours for OSAKA_COM`
* `Recent Holidays for OSAKA_COM`



Includes the following coverage:

#### OSAKA_COM -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            313 | 10.75%       |
| Futures Spread  |            731 | 25.1%        |
| Option          |           1868 | 64.15%       |
| Total           |           2912 | 100%         |


Consists of 3 Databases

* `OSAKA_COM`  - Tick Data
* `OSAKA_COM_BARS`  - 1 Minute Bars
* `OSAKA_COM_DAILY`  - End of Day Metrics




## OSAKA_COM

Database includes the following tick types:

* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## OSAKA_COM_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## OSAKA_COM_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


