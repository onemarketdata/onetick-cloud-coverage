# Global Corporate Actions History Schemas

Global Corporate Actions History




## OQD_CACT

Database includes the following tick types:

* CACT - Corporate Actions for All Securities



### OQD_CACT - CACT

Corporate Actions for All Securities

#### OQD_CACT - CACT Table Schema

| Field           | Data Type   | Description                                                                                                                                                                                                                            |
|-----------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME     | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP       | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OID             | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| ACTION_ID       | int         | Corporate Action Identifier                                                                                                                                                                                                            |
| ACTION_TYPE     | string[20]  | Corporate Action Type                                                                                                                                                                                                                  |
| ACTION_ADJUST   | double      | Corporate Action Adjustment Factor                                                                                                                                                                                                     |
| ACTION_CURRENCY | string[4]   | Currency for Corporate Action Payment                                                                                                                                                                                                  |
| ACTION_DATE     | int         | Corporate Action End Date                                                                                                                                                                                                              |
| DELETED_TIME    | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS     | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ          | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
