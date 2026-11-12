# Prague Stock Exchange

Trades, quotes, bars and book depth from the Prague Stock Exchange, the Czech Republic’s main stock exchange, with history from January 2014, covering Czech blue chips and international shares traded in Prague. Covered stocks include constituents of the PX index.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Czechia Czech Republic [CZ]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Prague
* Start Date: 20140102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: Prague Stock Exchange Index [TDI_IDX::PS]



Details are provided below

* `Table Schemas for PRAGUE`
* `Field Enumerations for PRAGUE`
* `Trading Hours for PRAGUE`
* `Recent Holidays for PRAGUE`



Includes the following coverage:

#### PRAGUE -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |            137 | 54.8%        |
| Convertible Bond   |              1 | 0.4%         |
| ETF                |              2 | 0.8%         |
| Equity             |             63 | 25.2%        |
| Investment Fund    |             36 | 14.4%        |
| Preferred Stock    |              1 | 0.4%         |
| Structured Product |             10 | 4.0%         |
| Total              |            250 | 100%         |


Consists of 3 Databases

* `PRAGUE`  - Tick Data
* `PRAGUE_BARS`  - 1 Minute Bars
* `PRAGUE_DAILY`  - End of Day Metrics




## PRAGUE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## PRAGUE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## PRAGUE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


