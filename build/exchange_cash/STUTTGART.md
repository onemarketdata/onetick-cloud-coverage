# Stuttgart Stock Exchange

Trades, quotes and bars from Boerse Stuttgart, Germany’s second-largest stock exchange, with history from January 2015. Boerse Stuttgart focuses on retail investors and is best known for structured products, with its Euwax segment one of Europe’s largest exchange segments for securitized derivatives. It also trades corporate bonds and uses market makers to quote a wide range of German and international shares, ETFs and funds.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Germany [DE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20150102
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: DAX Index [TDI_IDX::DA]



Details are provided below

* `Table Schemas for STUTTGART`
* `Field Enumerations for STUTTGART`
* `Trading Hours for STUTTGART`
* `Recent Holidays for STUTTGART`



Includes the following coverage:

#### STUTTGART -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |           5498 | 34.97%       |
| ETN             |              1 | 0.01%        |
| Equity          |          10156 | 64.59%       |
| Investment Fund |             28 | 0.18%        |
| Preferred Stock |             30 | 0.19%        |
| Right           |             10 | 0.06%        |
| Unknown         |              1 | 0.01%        |
| Total           |          15724 | 100%         |


Consists of 3 Databases

* `STUTTGART`  - Tick Data
* `STUTTGART_BARS`  - 1 Minute Bars
* `STUTTGART_DAILY`  - End of Day Metrics




## STUTTGART

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## STUTTGART_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## STUTTGART_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


