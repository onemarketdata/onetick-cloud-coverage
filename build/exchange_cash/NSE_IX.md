# NSE International Exchange

Trades, quotes, bars and book depth from NSE International Exchange (NSE IX) in GIFT City, India’s International Financial Services Centre, with history from August 2025. Trading is mainly in US dollars and includes derivatives on Indian indices and stocks, currency and commodity derivatives, depository receipts and US stocks. NSE IX is home to GIFT Nifty futures, the offshore NIFTY 50 contract that moved from SGX in 2023.

* Country: India [IN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Kolkata
* Start Date: 20250828
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: Nifty 50 [NSE_CASH::NIFTY50]



Details are provided below

* `Table Schemas for NSE_IX`
* `Field Enumerations for NSE_IX`
* `Trading Hours for NSE_IX`
* `Recent Holidays for NSE_IX`



Includes the following coverage:

#### NSE_IX -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             51 | 83.61%       |
| Future             |              4 | 6.56%        |
| Futures Spread     |              6 | 9.84%        |
| Total              |             61 | 100%         |


Consists of 3 Databases

* `NSE_IX`  - Tick Data
* `NSE_IX_BARS`  - 1 Minute Bars
* `NSE_IX_DAILY`  - End of Day Metrics




## NSE_IX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NSE_IX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## NSE_IX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


