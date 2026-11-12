# Tel Aviv Stock Exchange

Trades, quotes and bars from the Tel Aviv Stock Exchange (TASE), Israel’s only stock exchange, with history from July 2015, covering equities, futures, options and indices. TASE also trades corporate bonds, government bonds and treasury bills and index products such as ETFs. Index data includes the TA-35, the exchange’s flagship index of the 35 largest companies, and the broader TA-125.

* Country: Israel [IL]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tel_Aviv
* Start Date: 20150726
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: TA-35 [TEL_AVIV::2]



Details are provided below

* `Table Schemas for TEL_AVIV`
* `Field Enumerations for TEL_AVIV`
* `Trading Hours for TEL_AVIV`
* `Recent Holidays for TEL_AVIV`



Includes the following coverage:

#### TEL_AVIV -  Coverage

| Security Type    |   # of Symbols | % of Total   |
|------------------|----------------|--------------|
| Bond             |            138 | 1.23%        |
| Commercial Paper |             35 | 0.31%        |
| Commodity        |              1 | 0.01%        |
| Convertible Bond |             33 | 0.29%        |
| Corporate Bond   |            832 | 7.43%        |
| ETF              |            509 | 4.54%        |
| Equity           |            562 | 5.02%        |
| FX               |             14 | 0.12%        |
| Future           |             12 | 0.11%        |
| Government Bond  |             34 | 0.3%         |
| Index            |            129 | 1.15%        |
| Option           |           8809 | 78.64%       |
| Treasury Bill    |             13 | 0.12%        |
| Unknown          |              4 | 0.04%        |
| Warrant          |             76 | 0.68%        |
| Total            |          11201 | 100%         |


Consists of 3 Databases

* `TEL_AVIV`  - Tick Data
* `TEL_AVIV_BARS`  - 1 Minute Bars
* `TEL_AVIV_DAILY`  - End of Day Metrics




## TEL_AVIV

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TEL_AVIV_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TEL_AVIV_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


