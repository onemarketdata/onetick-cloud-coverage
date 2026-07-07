# TSX Venture Exchange

The TSX Venture Exchange is a Canadian stock exchange for emerging companies operated by the TMX Group.

* Country: Canada [CA]
* Mkt Hours: 09:00-16:00
* Time Zone: America/Toronto
* Start Date: 20171101
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for TSXV`
* `Field Enumerations for TSXV`
* `Trading Hours for TSXV`
* `Recent Holidays for TSXV`



Includes the following coverage:

#### TSXV -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Debenture       |              1 | 0.06%        |
| Equity          |           1682 | 95.9%        |
| Fund            |              2 | 0.11%        |
| Preferred Stock |              8 | 0.46%        |
| REIT            |              7 | 0.4%         |
| Right           |              3 | 0.17%        |
| Test            |              7 | 0.4%         |
| Unknown         |              1 | 0.06%        |
| Warrant         |             43 | 2.45%        |
| Total           |           1754 | 100%         |


Consists of 3 Databases

* `TSXV`  - Tick Data
* `TSXV_BARS`  - 1 Minute Bars
* `TSXV_DAILY`  - End of Day Metrics




## TSXV

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TSXV_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TSXV_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


