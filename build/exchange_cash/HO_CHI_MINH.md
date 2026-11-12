# Ho Chi Minh Stock Exchange

Trades, quotes and bars from the Ho Chi Minh Stock Exchange (HOSE), Vietnam’s largest stock exchange, with history from August 2011. It lists just over 400 companies and trades stocks, closed-end fund certificates, ETFs, covered warrants and bonds. Index data is included, covering the VN-Index, which tracks all HOSE-listed stocks, and the VN30 of the 30 largest companies.

* Country: Vietnam [VN]
* Mkt Hours: 08:00-17:00
* Time Zone: Asia/Ho_Chi_Minh
* Start Date: 20110829
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No
* Timestamp Type: Arrival
* Key Indices: VN-Index [HO_CHI_MINH::VNINDEX]



Details are provided below

* `Table Schemas for HO_CHI_MINH`
* `Field Enumerations for HO_CHI_MINH`
* `Trading Hours for HO_CHI_MINH`
* `Recent Holidays for HO_CHI_MINH`



Includes the following coverage:

#### HO_CHI_MINH -  Coverage

| Security Type   |   # of Symbols | % of Total   |
|-----------------|----------------|--------------|
| ETF             |             21 | 1.71%        |
| Equity          |            413 | 33.71%       |
| Index           |              1 | 0.08%        |
| Mutual Fund     |              4 | 0.33%        |
| Warrant         |            786 | 64.16%       |
| Total           |           1225 | 100%         |


Consists of 2 Databases

* `HO_CHI_MINH`  - Tick Data
* `HO_CHI_MINH_BARS`  - 1 Minute Bars




## HO_CHI_MINH

Database includes the following tick types:

* IDX - Index values
* LULD - Limit Up / Limit Down price levels
* MKT - Market phase / instrument status information
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## HO_CHI_MINH_BARS

Database includes the following tick types:

* MKT - Market phase / instrument status information
* QTE_1M - 1-minute quote bars
* TRD_1D - Daily trade bars
* TRD_1M - 1-minute trade bars
* VWAP_1H - 1-hour VWAP bars


