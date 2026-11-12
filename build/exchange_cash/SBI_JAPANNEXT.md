# Japannext J-Market

Trades, quotes, bars and book depth from Japannext’s J-Market, a proprietary trading system (PTS) for Japanese equities, with history from March 2014. Japannext is one of Japan’s main alternatives to the Tokyo Stock Exchange, often offering finer price increments for TSE-listed stocks. Covered stocks include Nikkei 225 and TOPIX constituents.

* Country: Japan [JP]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Tokyo
* Start Date: 20140318
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: Nikkei 225 Index [TDI_IDX::NE], TOPIX Index [TDI_IDX::TP]



Details are provided below

* `Table Schemas for SBI_JAPANNEXT`
* `Field Enumerations for SBI_JAPANNEXT`
* `Trading Hours for SBI_JAPANNEXT`
* `Recent Holidays for SBI_JAPANNEXT`



Includes the following coverage:

#### SBI_JAPANNEXT -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Total           |            476 | 100%         |


Consists of 2 Databases

* `SBI_JAPANNEXT`  - Tick Data
* `SBI_JAPANNEXT_BARS`  - 1 Minute Bars




## SBI_JAPANNEXT

Database includes the following tick types:

* MKT - Market phase / instrument status information
* PRL - Market depth data, aggregated by price point (MBP)
* QTE - Best bid / offer quotes
* TRD - Trades





## SBI_JAPANNEXT_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


