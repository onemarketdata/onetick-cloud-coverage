# Abu Dhabi Securities Exchange

Trades, quotes and bars from the Abu Dhabi Securities Exchange (ADX), with history from June 2016, covering equities, bonds, ETFs and futures of UAE companies. Index data is included, such as the FTSE ADX General Index (FADGI), the main benchmark for Abu Dhabi-listed stocks.

* Country: UAE [AE]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Dubai
* Start Date: 20160627
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: FTSE ADX 15 [ABU_DHABI::FADX15]



Details are provided below

* `Table Schemas for ABU_DHABI`
* `Field Enumerations for ABU_DHABI`
* `Trading Hours for ABU_DHABI`
* `Recent Holidays for ABU_DHABI`



Includes the following coverage:

#### ABU_DHABI -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |             24 | 13.11%       |
| Equity          |            105 | 57.38%       |
| Future          |             53 | 28.96%       |
| Index           |              1 | 0.55%        |
| Total           |            183 | 100%         |


Consists of 3 Databases

* `ABU_DHABI`  - Tick Data
* `ABU_DHABI_BARS`  - 1 Minute Bars
* `ABU_DHABI_DAILY`  - End of Day Metrics




## ABU_DHABI

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## ABU_DHABI_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## ABU_DHABI_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


