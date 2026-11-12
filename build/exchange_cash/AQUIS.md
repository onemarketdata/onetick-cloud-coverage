# Aquis UK

Trades, quotes, bars and book depth from Aquis Exchange UK, a pan-European MTF trading UK and European equities, with history from September 2016. Aquis is known for subscription-based pricing, where members pay according to message traffic rather than per trade, and it operates lit and dark books. It has been owned by SIX Group since July 2025. Covered stocks include constituents of the FTSE 100 and major European indices.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20160901
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for AQUIS`
* `Field Enumerations for AQUIS`
* `Trading Hours for AQUIS`
* `Recent Holidays for AQUIS`



Includes the following coverage:

#### AQUIS -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Unknown         |           7185 | 100.0%       |
| Total           |           7185 | 100%         |


Consists of 3 Databases

* `AQUIS`  - Tick Data
* `AQUIS_BARS`  - 1 Minute Bars
* `AQUIS_DAILY`  - End of Day Metrics




## AQUIS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## AQUIS_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## AQUIS_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


