# Taiwan Stock Exchange

Trades, quotes, bars and book depth from the Taiwan Stock Exchange (TWSE), Taiwan’s main board, with history from September 2014. It is home to major semiconductor companies such as TSMC. Covered stocks include constituents of the TAIEX and FTSE TWSE Taiwan 50; index values are in TWSE_IDX.  A consolidated tape for both Taiwanese equity markets is provided in the TW_COMP dataset.

* Country: Taiwan [TW]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Taipei
* Start Date: 20140901
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: TAIEX [TWSE_IDX::IX0001], FTSE TWSE Taiwan 50 [TWSE_IDX::TW50]



Details are provided below

* `Table Schemas for TWSE`
* `Field Enumerations for TWSE`
* `Trading Hours for TWSE`
* `Recent Holidays for TWSE`



Includes the following coverage:

#### TWSE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              6 | 0.02%        |
| ETF                |            229 | 0.58%        |
| ETN                |             15 | 0.04%        |
| Equity             |           1103 | 2.77%        |
| Government Bond    |            148 | 0.37%        |
| Preferred Stock    |             27 | 0.07%        |
| REIT               |              6 | 0.02%        |
| Structured Product |          38273 | 96.15%       |
| Total              |          39807 | 100%         |


Consists of 3 Databases

* `TWSE`  - Tick Data
* `TWSE_BARS`  - 1 Minute Bars
* `TWSE_DAILY`  - End of Day Metrics




## TWSE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* PRL_ODD_LOT - Odd lot orderbook data, for exchanges that have a separate book for odd lots
* QTE - Best bid / offer quotes
* QTE_ODD_LOT - BBO quotes from the Odd Lot book, for exchanges that have a separate order book for odd lots
* TRD - Trades





## TWSE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TWSE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


