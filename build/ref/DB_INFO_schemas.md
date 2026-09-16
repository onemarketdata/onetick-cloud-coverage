# Database Daily Archive Loading Statistics Schemas

Database Daily Archive Loading Statististics. Keyed on Database




## DB_INFO

Database includes the following tick types:

* COMPLETENESS - Database Loading Statistics by Table / Tick Type
* PROC_EVENTS - Database Daily Loading Events including Start and Completion Time



### DB_INFO - COMPLETENESS

Database Loading Statistics by Table / Tick Type

#### DB_INFO - COMPLETENESS Table Schema

| Field                 | Data Type    | Description                                                                                                                                                                                                                            |
|-----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME           | string       | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP             | nsectime     | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| DB_NAME               | string[100]  | Database Name                                                                                                                                                                                                                          |
| DB_DESCRIPTION        | string[250]  | Database Description                                                                                                                                                                                                                   |
| MIC                   | string[1500] | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded                                                                                                                                       |
| COUNTRY               | string[70]   | ISO Country Code                                                                                                                                                                                                                       |
| TIMEZONE              | string[25]   | Time Zone for the Database                                                                                                                                                                                                             |
| MARKET_START          | string[29]   | Daily Start Time for Trading                                                                                                                                                                                                           |
| MARKET_END            | string[29]   | Daily End Time for Trading                                                                                                                                                                                                             |
| DATA_DATE             | string[8]    | Trading Day loaded, which may not correspond to a UTC Day.                                                                                                                                                                             |
| DAILY_ARCHIVE_SIZE_MB | long         | Daily Archive Size in Mb                                                                                                                                                                                                               |
| TICK_TYPE             | string[25]   | Database Table                                                                                                                                                                                                                         |
| SYMBOL_COUNT          | long         | Count of Symbols loaded into the Database Table for the specified day.                                                                                                                                                                 |
| LOWEST_TIMESTAMP      | msectime     | Highest Timestamp loaded for the specified day                                                                                                                                                                                         |
| HIGHEST_TIMESTAMP     | msectime     | Highest Timestamp loaded for the specified day                                                                                                                                                                                         |
| LOAD_TIME             | msectime     | Timestamp the historic day of data was loaded into the database                                                                                                                                                                        |
| REF_DATA_DB           | string[100]  | Reference Database associated with a Database.  Used to provide symbology mapping, corporate action adjustment factors, mkt holidays and trading hours                                                                                 |
| SYMBOLOGY             | string[15]   | Symbology assigned to the Database                                                                                                                                                                                                     |
| EQUITIES              | string[4]    | If the Database includes Equities [ Y / N ]                                                                                                                                                                                            |
| FUTURES               | string[4]    | If the Database includes Futures [ Y / N ]                                                                                                                                                                                             |
| OPTIONS               | string[4]    | If the Database includes Options [ Y / N ]                                                                                                                                                                                             |
| SPREADS               | string[4]    | If the Database includes Future Spread Contracts [ Y / N ]                                                                                                                                                                             |
| INDICES               | string[4]    | If the Database includes Indices [ Y / N ]                                                                                                                                                                                             |
| COMMENT               | string[250]  | Commentary                                                                                                                                                                                                                             |
| OMDSEQ                | uint         | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |

### DB_INFO - PROC_EVENTS

Database Daily Loading Events including Start and Completion Time

#### DB_INFO - PROC_EVENTS Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME      | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP        | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| DB_NAME          | string[100] | Database Name                                                                                                                                                                                                                          |
| DB_DESCRIPTION   | string[250] | Database Description                                                                                                                                                                                                                   |
| TIMEZONE         | string[25]  | Time Zone for the Database                                                                                                                                                                                                             |
| DATA_DATE        | string[8]   | Trading Day loaded, which may not correspond to a UTC Day.                                                                                                                                                                             |
| EVENT_TIME       | msectime    | Timestamp for Event                                                                                                                                                                                                                    |
| EVENT_NAME       | string[50]  | Event Name                                                                                                                                                                                                                             |
| SOURCE_FILE_NAME | string[200] | Category of Daily Database Loading                                                                                                                                                                                                     |
| OMDSEQ           | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
