# Nasdaq Nordic (Stockholm, Copenhagen, Helsinki, Iceland) - Equities

Nasdaq Nordic operates the stock exchanges in Stockholm, Copenhagen, Helsinki and Iceland facilitating trading in Nordic equities.

* Country: Sweden Denmark Finland Iceland [SE DK FI IS]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Stockholm
* Start Date: 20081021
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for NORDIC_EQ`
* `Field Enumerations for NORDIC_EQ`
* `Trading Hours for NORDIC_EQ`
* `Recent Holidays for NORDIC_EQ`



Includes the following coverage:

#### NORDIC_EQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |             63 | 2.89%        |
| Depository Receipt |              6 | 0.28%        |
| ETF                |             32 | 1.47%        |
| ETN                |             16 | 0.73%        |
| Equity             |           1438 | 65.96%       |
| Investment Fund    |            496 | 22.75%       |
| Preferred Stock    |              9 | 0.41%        |
| Right              |             28 | 1.28%        |
| Unknown            |             92 | 4.22%        |
| Total              |           2180 | 100%         |


Consists of 4 Databases

* `NORDIC_EQ`  - Tick Data
* `NORDIC_EQ_BARS`  - 1 Minute Bars
* `NORDIC_EQ_DAILY`  - End of Day Metrics
* `NORDIC_EQ_LATEST`  - Real Time Latest Values




## NORDIC_EQ

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NORDIC_EQ_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## NORDIC_EQ_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## NORDIC_EQ_LATEST

Database includes the following tick types:

* TRD - Trades
* QTE - Best bid / offer quotes


