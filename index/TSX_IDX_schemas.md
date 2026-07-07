# Toronto Stock Exchange - Indices Schemas

The Toronto Stock Exchange ( TSX ) provides various indices tracking the performance of Canadian equities, including the S&P/TSX Composite Index and sector-specific indices.




## TSX_IDX

Database includes the following tick types:

* IDX - Index values
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type



### TSX_IDX - IDX

Index values

#### TSX_IDX - IDX Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCH_TIME | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
| PRICE     | double      | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross                              |

### TSX_IDX - QTE

Best bid / offer quotes

#### TSX_IDX - QTE Table Schema

| Field     | Data Type   | Description                                                                                                                                                                                                                            |
|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_PRICE | double      | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)                                                                                                       |
| BID_PRICE | double      | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)                                                                                                       |
| OMDSEQ    | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
