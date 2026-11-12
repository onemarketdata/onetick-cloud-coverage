# Bybit

Trades, Quotes and Book depth from Bybit, the second-largest cryptocurrency exchange by volume, with spot and futures from August 2024 and options from September 2026. Bybit is especially active in USDT perpetual contracts and also offers staking and P2P trading.

* Country: Global [Global]
* Mkt Hours: 00:00-24:00
* Time Zone: UTC
* Start Date: 20240822 - Spots & Futures, 20260908 - Options
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices:



Details are provided below

* `Table Schemas for BYBIT`
* `Field Enumerations for BYBIT`
* `Trading Hours for BYBIT`
* `Recent Holidays for BYBIT`



Includes the following coverage:

#### BYBIT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| FX Spot         |            527 | 5.66%        |
| Future          |            936 | 10.05%       |
| Option          |           7854 | 84.3%        |
| Total           |           9317 | 100%         |


Consists of 2 Databases

* ```
  `BYBIT`_
  ```

    - Tick Data
* `BYBIT_DAILY`  - End of Day Metrics




## BYBIT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## BYBIT_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


