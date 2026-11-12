# National Stock Exchange of India - Equities

Trades, quotes, bars and book depth from the National Stock Exchange of India (NSE) equity market, India’s largest stock exchange by turnover, with history from January 2012. Index data includes the NIFTY 50 and other NIFTY indices.

* Country: India [IN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Kolkata
* Start Date: 20120102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: Nifty 50 [NSE_CASH::NIFTY50]



Details are provided below

* `Table Schemas for NSE_CASH`
* `Field Enumerations for NSE_CASH`
* `Trading Hours for NSE_CASH`
* `Recent Holidays for NSE_CASH`



Includes the following coverage:

#### NSE_CASH -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |           2160 | 100%         |


Consists of 2 Databases

* `NSE_CASH`  - Tick Data
* `NSE_CASH_BARS`  - 1 Minute Bars




## NSE_CASH

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* TRD - Trades





## NSE_CASH_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


