# Turquoise UK

Trades, quotes and bars from Turquoise, a pan-European multilateral trading facility (MTF) owned by the London Stock Exchange Group, with history from October 2010. Founded in 2008 by a group of investment banks, Turquoise offers trading in UK, Swiss, US and European shares, ETFs and depositary receipts through Turquoise UK in London and Turquoise Europe in Amsterdam. It is known for its lit order book and its block trading services, formerly Turquoise Plato and now branded Turquoise Dark.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20101004
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for TURQUOISE`
* `Field Enumerations for TURQUOISE`
* `Trading Hours for TURQUOISE`
* `Recent Holidays for TURQUOISE`



Includes the following coverage:

#### TURQUOISE -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |            926 | 23.43%       |
| Equity          |           3023 | 76.49%       |
| Unknown         |              3 | 0.08%        |
| Total           |           3952 | 100%         |


Consists of 3 Databases

* `TURQUOISE`  - Tick Data
* `TURQUOISE_BARS`  - 1 Minute Bars
* `TURQUOISE_DAILY`  - End of Day Metrics




## TURQUOISE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TURQUOISE_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TURQUOISE_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


