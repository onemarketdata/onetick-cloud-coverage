# India Consolidated Equities

Consolidated trades, NBBO, exchange quotes and bars for Indian equities from the National Stock Exchange of India (NSE) and BSE, including the BSE SME platform, with history from January 2012. It lets you analyse Indian stocks across both major exchanges in one database. Covered stocks include constituents of the NIFTY 50 and BSE SENSEX.

* Country: India [IN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Kolkata
* Start Date: 20120102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: Nifty 50 [NSE_CASH::NIFTY50]



Details are provided below

* `Table Schemas for IN_COMP`
* `Field Enumerations for IN_COMP`
* `Trading Hours for IN_COMP`
* `Recent Holidays for IN_COMP`



Includes the following coverage:

#### IN_COMP -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |            108 | 1.52%        |
| Equity          |           6742 | 94.97%       |
| Unknown         |            249 | 3.51%        |
| Total           |           7099 | 100%         |


Consists of 3 Databases

* `IN_COMP`  - Tick Data
* `IN_COMP_BARS`  - 1 Minute Bars
* `IN_COMP_DAILY`  - End of Day Metrics




## IN_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## IN_COMP_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## IN_COMP_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


