# Tokyo Financial Exchange

Futures and spreads with Trades, Quotes and bars from the Tokyo Financial Exchange (TFX), with history from August 2019. TFX lists yen short-term interest rate futures such as three-month Euroyen futures, plus exchange-traded FX margin (Click 365) and equity index (Click Kabu 365) contracts popular with Japanese retail traders.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20190809
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for TFX`
* `Field Enumerations for TFX`
* `Trading Hours for TFX`
* `Recent Holidays for TFX`



Includes the following coverage:

#### TFX -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Future          |             37 | 12.63%       |
| Futures Spread  |            256 | 87.37%       |
| Total           |            293 | 100%         |


Consists of 3 Databases

* `TFX`  - Tick Data
* `TFX_BARS`  - 1 Minute Bars
* `TFX_DAILY`  - End of Day Metrics




## TFX

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## TFX_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## TFX_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


