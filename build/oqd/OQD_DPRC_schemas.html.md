# Daily Price History for Global Equities Schemas

Daily Price History for Global Equities




## OQD_DPRC

Database includes the following tick types:

* DPRC - Daily Prices



### OQD_DPRC - DPRC

Daily Prices

#### OQD_DPRC - DPRC Table Schema

| Field        | Data Type   | Description                                                                                                                                                                                                                            |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLOSE        | double      | Closing price                                                                                                                                                                                                                          |
| CLOSE        | double      | Closing price                                                                                                                                                                                                                          |
| CURRENCY     | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| CURRENCY     | string[3]   | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).                                                                                                                        |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| DELETED_TIME | msectime    | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                       |
| EXCH         | string[10]  | Exchange from which the update originates (Country Code + [MIC or PRIM for Primary, or COMP for Composite])                                                                                                                            |
| EXCH         | string[10]  | Exchange from which the update originates (Country Code + [MIC or PRIM for Primary, or COMP for Composite])                                                                                                                            |
| HIGH         | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| HIGH         | double      | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval                                                                                                            |
| LOW          | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| LOW          | double      | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval                                                                                                             |
| OID          | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| OID          | string[14]  | OneMarketData ID                                                                                                                                                                                                                       |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OMDSEQ       | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| OPEN         | double      | Open price for the current trading day                                                                                                                                                                                                 |
| OPEN         | double      | Open price for the current trading day                                                                                                                                                                                                 |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| TICK_STATUS  | int         | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).                                                                                                                                           |
| VOLUME       | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
| VOLUME       | double      | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval                                                                                                      |
