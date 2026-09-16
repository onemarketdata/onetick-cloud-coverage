# Symbol Universe for all databases Schemas

Symbol Universe for all databases. Keyed on Database and Security Type.




## SYMBOL_UNIVERSE

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type



### SYMBOL_UNIVERSE - STAT

Static data, e.g. ISIN, description, security type

#### SYMBOL_UNIVERSE - STAT Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                                |
|---------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                             |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                    |
| STRIKE_PRICE        | double      | Exercise price for options / warrants                                                                                                                                                                                                      |
| CONTRACT_SIZE       | double      | Indicates a derivative’s underlying quantity                                                                                                                                                                                               |
| TICK_VALUE          | double      | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.                                                                                                                                        |
| DB_NAME             | string[20]  | Database Name                                                                                                                                                                                                                              |
| NAME                | string[250] | Description of the instrument                                                                                                                                                                                                              |
| EXCH_SYMBOL         | string[100] | Ticker symbol specified by the exchange                                                                                                                                                                                                    |
| DB_SYMBOL           | string[100] | Identifies the symbol used in the source database.                                                                                                                                                                                         |
| OID                 | string[100] | OneMarketData ID                                                                                                                                                                                                                           |
| BSYM                | string[100] | Bloomberg Symbol                                                                                                                                                                                                                           |
| FGC                 | string[100] |                                                                                                                                                                                                                                            |
| SECTOR              | string[300] |                                                                                                                                                                                                                                            |
| ISIN                | string[20]  | ISIN code                                                                                                                                                                                                                                  |
| TRADING_CODE        | string[30]  | ID used to identify the instrument in the trading system                                                                                                                                                                                   |
| MIC                 | string[10]  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                           |
| OPERATING_MIC       | string[10]  | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded                                                                                                                         |
| SEC_TYPE            | string[30]  | Security type, e.g. Equity, ETF, Future                                                                                                                                                                                                    |
| CFI_CODE            | string[10]  | Classification of Financial Instruments code (ISO 10962), indicating the type of security                                                                                                                                                  |
| MKT_SEGMENT         | string[60]  | Market segment on which the instrument is traded                                                                                                                                                                                           |
| CURRENCY            | string[10]  | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                            |
| EXPIRATION_DATE     | string[10]  | Date when a derivative expires (YYYYMMDD)                                                                                                                                                                                                  |
| CALL_PUT_IND        | string[2]   | C - Call option, P - Put option                                                                                                                                                                                                            |
| PRODUCT_CODE        | string[30]  | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD. |
| STRATEGY_TYPE       | string[50]  | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly                                                                                                                                                                         |
| UNDERLYING_SYMBOL   | string[20]  | Symbol of the underlying instrument                                                                                                                                                                                                        |
| SIP_SYMBOL          | string[50]  | Ticker symbol used by the US Securities Information Processor (CTA / UTP)                                                                                                                                                                  |
| TICK_SIZE           | string[50]  | Tick size / minimum price increment. All order prices must be a multiple of the tick size.                                                                                                                                                 |
| UNDERLYING_SEC_TYPE | string[20]  | Underlying asset class                                                                                                                                                                                                                     |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.     |
