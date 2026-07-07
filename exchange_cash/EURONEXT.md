# Euronext (Paris / Amsterdam / Brussels / Lisbon / ETFs + Funds / Best of Book)

Euronext operates regulated exchanges in Paris, Amsterdam, Brussels, and Lisbon, facilitating trading in equities, ETFs, warrants, certificates, bonds, derivatives, commodities, and indices.

* Country: France Netherlands Belgium Portugal [FR NL BE PT IT NO IE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20120102
* Real Time Available: Yes
* Bars Available: Yes
* Book Depth Available: Yes



Details are provided below

* `Table Schemas for EURONEXT`
* `Field Enumerations for EURONEXT`
* `Trading Hours for EURONEXT`
* `Recent Holidays for EURONEXT`



Includes the following coverage:

#### EURONEXT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |          11151 | 79.17%       |
| ETF             |           1714 | 12.17%       |
| Equity          |           1214 | 8.62%        |
| Test            |              6 | 0.04%        |
| Total           |          14085 | 100%         |


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



