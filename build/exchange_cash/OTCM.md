# OTC Markets (US OTC Quotes)

Quotes, trades, bars and book depth from OTC Markets Group’s OTC Link ATS, an SEC-registered alternative trading system, with history from July 2018, covering about 12,000 US and international securities on the OTCQX, OTCQB, OTCID and Pink markets. It is the main source for US OTC quotes, including many ADRs and foreign ordinary shares of large non-US companies.

* Country: USA United States [US]
* Mkt Hours: 09:30-16:00
* Time Zone: America/New_York
* Start Date: 20180712
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: Yes
* Timestamp Type: Exchange (Publication)
* Key Indices: S&P 500 Index [TDI_IDX::SP], Dow Jones Industrial Average Index [TDI_IDX::DJ], NASDAQ 100 Index [TDI_IDX::ND], NASDAQ Composite Index [TDI_IDX::NC]



Details are provided below

* `Table Schemas for OTCM`
* `Field Enumerations for OTCM`
* `Trading Hours for OTCM`
* `Recent Holidays for OTCM`



Includes the following coverage:

#### OTCM -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| Unknown         |          13004 | 100.0%       |
| Total           |          13004 | 100%         |


Consists of 2 Databases

* `OTCM`  - Tick Data
* `OTCM_BARS`  - 1 Minute Bars




## OTCM

Database includes the following tick types:

* BBO - Combined best bid / offer quotes calculated across multiple sources
* OTCM_INSIDE_QTE - OTCM Inside Quote
* STAT - Static data, e.g. ISIN, description, security type





## OTCM_BARS

Database includes the following tick types:

* QTE_1M - 1-minute quote bars


