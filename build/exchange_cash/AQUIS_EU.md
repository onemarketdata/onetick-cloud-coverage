# Aquis Europe

Trades, quotes, bars and book depth from Aquis Exchange Europe, the Paris-based EU MTF that Aquis set up after Brexit, with history from September 2019. It trades equities from European markets outside the UK and uses the same subscription pricing model as Aquis UK. Aquis has been owned by SIX Group since July 2025. Covered stocks include constituents of the EURO STOXX 50, DAX and CAC 40.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/London
* Start Date: 20190930
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Matching Engine)
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for AQUIS_EU`
* `Field Enumerations for AQUIS_EU`
* `Trading Hours for AQUIS_EU`
* `Recent Holidays for AQUIS_EU`



Includes the following coverage:

#### AQUIS_EU -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Unknown         |           4149 | 100.0%       |
| Total           |           4149 | 100%         |


Consists of 3 Databases

* `AQUIS_EU`  - Tick Data
* `AQUIS_EU_BARS`  - 1 Minute Bars
* `AQUIS_EU_DAILY`  - End of Day Metrics




## AQUIS_EU

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* IND - Indicative pricing, e.g. indicative auction prices and imbalance
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## AQUIS_EU_BARS

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars





## AQUIS_EU_DAILY

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type


