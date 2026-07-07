# Korea Exchange - Indices Schemas

Korea Exchange offers trading in major Korean equity indices like the KOSPI, KOSDAQ and sector/strategy indices.




## KOREA_IDX

Database includes the following tick types:

* IDX - Index values
* STAT - Static data, e.g. ISIN, description, security type



### KOREA_IDX - IDX

Index values

#### KOREA_IDX - IDX Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
