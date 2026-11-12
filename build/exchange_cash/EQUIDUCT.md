# Equiduct Exchange

Trades, Quotes and Book depth from Equiduct, a pan-European trading venue operated as a market segment of Börse Berlin, with history from October 2015. Equiduct focuses on retail order flow: market makers execute retail brokers’ orders at or better than a European best bid and offer built from the main European venues, covering Europe’s most liquid equities and ETFs. This makes it useful for studying retail execution quality in stocks such as EURO STOXX 50 and FTSE 100 constituents.  A consolidated tape for all European equity markets is provided in the EU_COMP dataset.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Berlin
* Start Date: 20151023
* Real Time Available: No
* Bars Available: No
* Book Depth Available: Yes
* Timestamp Type: Arrival
* Key Indices: STOXX 50 Index [TDI_IDX::VH], Euro STOXX 50 Index [TDI_IDX::XX]



Details are provided below

* `Table Schemas for EQUIDUCT`
* `Field Enumerations for EQUIDUCT`
* `Trading Hours for EQUIDUCT`
* `Recent Holidays for EQUIDUCT`



Includes the following coverage:

#### EQUIDUCT -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Depository Receipt |              6 | 0.24%        |
| ETC                |              2 | 0.08%        |
| ETF                |             34 | 1.33%        |
| Equity             |           2502 | 98.08%       |
| REIT               |              7 | 0.27%        |
| Total              |           2551 | 100%         |


Consists of 1 Databases

* `EQUIDUCT`  - Tick Data




## EQUIDUCT

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* MKT - Market phase / instrument status information
* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades


