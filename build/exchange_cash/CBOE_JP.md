# Cboe Japan

Trades, quotes and bars from Cboe Japan (formerly Chi-X Japan), a proprietary trading system (PTS) that offered an alternative to the Tokyo Stock Exchange for Japanese equities and ETFs, with history from April 2014. Cboe ceased its Japanese equities operations in August 2025. It is useful for studying PTS market share and execution quality in Japanese stocks such as Nikkei 225 and TOPIX constituents.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20140421
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type:
* Key Indices: Nikkei 225 Index [TDI_IDX::NE], TOPIX Index [TDI_IDX::TP]



Details are provided below

* `Table Schemas for CBOE_JP`
* `Field Enumerations for CBOE_JP`
* `Trading Hours for CBOE_JP`
* `Recent Holidays for CBOE_JP`



Includes the following coverage:

#### CBOE_JP -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |           3655 | 100%         |


Consists of 3 Databases

* `CBOE_JP`  - Tick Data
* `CBOE_JP_BARS`  - 1 Minute Bars
* `CBOE_JP_DAILY`  - End of Day Metrics




## CBOE_JP

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## CBOE_JP_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## CBOE_JP_DAILY

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type


