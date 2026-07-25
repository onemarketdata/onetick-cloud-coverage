# New Zealand Exchange (NZX)

The NZX is New Zealand’s main securities exchange trading equities, bonds and other products.

* Country: New Zealand [NZ]
* Mkt Hours: 08:00-17:00
* Time Zone: Australia/Sydney
* Start Date: 20141202
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for NZX`
* `Field Enumerations for NZX`
* `Trading Hours for NZX`
* `Recent Holidays for NZX`



Includes the following coverage:

#### NZX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Bond            |             17 | 8.63%        |
| ETF             |             44 | 22.34%       |
| Equity          |            124 | 62.94%       |
| Fund            |              5 | 2.54%        |
| Preferred Stock |              1 | 0.51%        |
| Warrant         |              6 | 3.05%        |
| Total           |            197 | 100%         |


Consists of 3 Databases

* `NZX`  - Tick Data
* `NZX_BARS`  - 1 Minute Bars
* `NZX_DAILY`  - End of Day Metrics




## NZX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NZX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## NZX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type
* TRD_1D - Daily trade bars


