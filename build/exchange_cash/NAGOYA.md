# Nagoya Stock Exchange

Trades, quotes and bars from the Nagoya Stock Exchange, with history from November 2009, covering its Premier, Main and Next markets. Many companies from the Chubu industrial region are listed there, often alongside a Tokyo listing. For consolidated Japanese data, use JP_COMP.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20091109
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: Nikkei 225 Index [TDI_IDX::NE], TOPIX Index [TDI_IDX::TP]



Details are provided below

* `Table Schemas for NAGOYA`
* `Field Enumerations for NAGOYA`
* `Trading Hours for NAGOYA`
* `Recent Holidays for NAGOYA`



Includes the following coverage:

#### NAGOYA -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |              2 | 0.62%        |
| Equity          |            323 | 99.38%       |
| Total           |            325 | 100%         |


Consists of 2 Databases

* `NAGOYA`  - Tick Data
* `NAGOYA_BARS`  - 1 Minute Bars




## NAGOYA

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## NAGOYA_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


