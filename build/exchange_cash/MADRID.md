# Madrid Stock Exchange (SIBE)

The Madrid Stock Exchange is one of four regional stock exchanges in Spain that make up the overall Spanish stock market.

* Country: Spain [ES]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Madrid
* Start Date: 20120102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for MADRID`
* `Field Enumerations for MADRID`
* `Trading Hours for MADRID`
* `Recent Holidays for MADRID`



Includes the following coverage:

#### MADRID -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Certificate     |           2299 | 72.75%       |
| ETF             |              7 | 0.22%        |
| Equity          |            355 | 11.23%       |
| Investment Fund |            496 | 15.7%        |
| Right           |              3 | 0.09%        |
| Total           |           3160 | 100%         |


Consists of 4 Databases

* `MADRID`  - Tick Data
* `MADRID_BARS`  - 1 Minute Bars
* `MADRID_DAILY`  - End of Day Metrics
* `MADRID_LATEST`  - Real Time Latest Values




## MADRID

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IDX - Index values
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* NAV - Net Asset Value for investment funds
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## MADRID_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## MADRID_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## MADRID_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


