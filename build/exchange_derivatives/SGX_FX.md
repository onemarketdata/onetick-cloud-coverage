# Singapore Exchange - FX Derivatives

Futures and spreads with Trades, Quotes and bars for SGX FX futures, with history from September 2014. SGX is one of Asia’s largest FX futures exchanges, with key contracts in USD/CNH, INR/USD and other Asian currency pairs.

* Country: Singapore [SG]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Singapore
* Start Date: 20140908
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for SGX_FX`
* `Field Enumerations for SGX_FX`
* `Trading Hours for SGX_FX`
* `Recent Holidays for SGX_FX`



Includes the following coverage:

#### SGX_FX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |            391 | 27.79%       |
| Futures Spread  |           1016 | 72.21%       |
| Total           |           1407 | 100%         |


Consists of 3 Databases

* `SGX_FX`  - Tick Data
* `SGX_FX_BARS`  - 1 Minute Bars
* `SGX_FX_DAILY`  - End of Day Metrics




## SGX_FX

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## SGX_FX_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## SGX_FX_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


