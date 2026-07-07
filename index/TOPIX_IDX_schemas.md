# TOPIX Indices Schemas

TOPIX Indices are a series of stock market indices for the Tokyo Stock Exchange, including the TOPIX, which tracks the performance of all domestic companies in the First Section of the TSE.




## TOPIX_IDX

Database includes the following tick types:

* IDX - Index values
* STAT - Static data, e.g. ISIN, description, security type



### TOPIX_IDX - IDX

Index values

#### TOPIX_IDX - IDX Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE     | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |
