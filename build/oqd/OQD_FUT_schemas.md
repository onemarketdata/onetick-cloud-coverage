# Daily Price History for Global Futures Schemas

Daily Price History for Global Futures




## OQD_FUT

Database includes the following tick types:

* DFUT - Daily Futures Prices



### OQD_FUT - DFUT

Daily Futures Prices

#### OQD_FUT - DFUT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                            |
|-------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME       | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP         | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| OPEN              | double      | Open price for the current trading day                                                                                                                                                                                                 |
| HIGH              | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW               | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| SETTLE_PRICE      | double      | Settlement price                                                                                                                                                                                                                       |
| VOLUME            | long        | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| OPEN_INT          | double      | Open interest for futures / options                                                                                                                                                                                                    |
| OPEN_INT_AT_CLOSE | double      | Open Interest at market close                                                                                                                                                                                                          |
| DELETED_TIME      | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| TICK_STATUS       | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| OMDSEQ            | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
