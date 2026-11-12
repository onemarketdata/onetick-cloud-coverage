# Nasdaq Nordic (Stockholm, Copenhagen, Helsinki, Iceland) - Equities

Trades, quotes, bars and book depth, with real-time data, from Nasdaq’s Nordic exchanges in Stockholm, Copenhagen, Helsinki and Iceland, with history from October 2008, including First North Growth Market for smaller companies. Covered stocks include constituents of the OMX Stockholm 30, OMX Copenhagen 25 and OMX Helsinki 25; index values are in NORDIC_IDX. A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Sweden Denmark Finland Iceland [SE DK FI IS]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Stockholm
* Start Date: 20081021
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: OMX All-Share Stockholm Index [TDI_IDX::SM], OMX Copenhagen Index [TDI_IDX::KA], OMX Helsinki 25 Index [TDI_IDX::HE]



Details are provided below

* `Table Schemas for NORDIC_EQ`
* `Field Enumerations for NORDIC_EQ`
* `Trading Hours for NORDIC_EQ`
* `Recent Holidays for NORDIC_EQ`



Includes the following coverage:

#### NORDIC_EQ -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |             65 | 3.01%        |
| Depository Receipt |              5 | 0.23%        |
| ETF                |             32 | 1.48%        |
| ETN                |             16 | 0.74%        |
| Equity             |           1429 | 66.16%       |
| Investment Fund    |            496 | 22.96%       |
| Preferred Stock    |              9 | 0.42%        |
| Right              |             14 | 0.65%        |
| Unknown            |             94 | 4.35%        |
| Total              |           2160 | 100%         |


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

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


