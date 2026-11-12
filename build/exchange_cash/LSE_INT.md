# London Stock Exchange - International Market

Trades, quotes, bars and book depth from the London Stock Exchange’s International Order Book (IOB), with history from May 2012. The IOB trades depositary receipts of companies from more than 60 countries, many of them in emerging markets, giving international investors access to these companies in London during UK trading hours.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: UK United Kindom [GB]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20120531
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for LSE_INT`
* `Field Enumerations for LSE_INT`
* `Trading Hours for LSE_INT`
* `Recent Holidays for LSE_INT`



Includes the following coverage:

#### LSE_INT -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |             70 | 5.85%        |
| ETF                |            175 | 14.62%       |
| ETN                |              4 | 0.33%        |
| Equity             |            948 | 79.2%        |
| Total              |           1197 | 100%         |


Consists of 3 Databases

* `LSE_INT`  - Tick Data
* `LSE_INT_BARS`  - 1 Minute Bars
* `LSE_INT_DAILY`  - End of Day Metrics




## LSE_INT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## LSE_INT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## LSE_INT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


