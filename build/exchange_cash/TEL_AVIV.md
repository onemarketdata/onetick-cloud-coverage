# Tel Aviv Stock Exchange

The Tel Aviv Stock Exchange is Israel’s only stock exchange. It trades shares, corporate bonds, treasury bills, index products and derivatives

* Country: Israel [IL]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tel_Aviv
* Start Date: 20150726
* Real Time Available: No
* Bars Available: No
* Book Depth Available: No



Details are provided below

* `Table Schemas for TEL_AVIV`
* `Field Enumerations for TEL_AVIV`
* `Trading Hours for TEL_AVIV`
* `Recent Holidays for TEL_AVIV`



Includes the following coverage:

#### TEL_AVIV -  Coverage

| Security Type    |   # of Symbols | % of Total   |
|------------------|----------------|--------------|
| Bond             |            129 | 1.13%        |
| Commercial Paper |             30 | 0.26%        |
| Commodity        |              1 | 0.01%        |
| Convertible Bond |             36 | 0.32%        |
| Corporate Bond   |            846 | 7.43%        |
| ETF              |            504 | 4.42%        |
| Equity           |            560 | 4.92%        |
| FX               |             14 | 0.12%        |
| Future           |             12 | 0.11%        |
| Government Bond  |             35 | 0.31%        |
| Index            |            127 | 1.12%        |
| Option           |           9000 | 79.02%       |
| Treasury Bill    |             13 | 0.11%        |
| Unknown          |              5 | 0.04%        |
| Warrant          |             78 | 0.68%        |
| Total            |          11390 | 100%         |


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
* TRD_1D - Daily trade bars


