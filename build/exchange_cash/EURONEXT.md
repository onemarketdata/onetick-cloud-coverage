# Euronext (Paris / Amsterdam / Brussels / Lisbon / ETFs + Funds / Best of Book)

Trades, quotes, bars and book depth, with real-time data, from Euronext’s cash markets in Paris, Amsterdam, Brussels, Lisbon, Oslo and Dublin, with history from January 2012, including Euronext Growth and Access segments, ETFs, funds and best-of-book data. Euronext runs a single order book platform across its markets, so all of these venues can be analysed together. Covered stocks include constituents of the CAC 40, AEX, BEL 20, PSI, OBX and ISEQ 20.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: France Netherlands Belgium Portugal [FR NL BE PT IT NO IE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: CAC 40 Index [TDI_IDX::CF], Amsterdam AEX Index [TDI_IDX::AE], BEL 20 Index [TDI_IDX::BE], PSI 20 Index [TDI_IDX::PP]



Details are provided below

* `Table Schemas for EURONEXT`
* `Field Enumerations for EURONEXT`
* `Trading Hours for EURONEXT`
* `Recent Holidays for EURONEXT`



Includes the following coverage:

#### EURONEXT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |          11293 | 79.11%       |
| ETF             |           1774 | 12.43%       |
| Equity          |           1202 | 8.42%        |
| Test            |              6 | 0.04%        |
| Total           |          14275 | 100%         |


Consists of 4 Databases

* `EURONEXT`  - Tick Data
* `EURONEXT_BARS`  - 1 Minute Bars
* `EURONEXT_DAILY`  - End of Day Metrics
* `EURONEXT_LATEST`  - Real Time Latest Values




## EURONEXT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* REF_PRICE - Benchmark / reference prices
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EURONEXT_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* LAT_1M - 1-minute Latency bars for real time delivered data
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## EURONEXT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type





## EURONEXT_LATEST

Database includes the following tick types:

* SNAP - Latest Trade & Quote / NBBO Prices for all Instruments in the venue
* SNAP_QTE - Latest Quotes for all Instruments in the venue
* SNAP_TRD - Latest Trade Prices for all Traded Instruments in the venue


