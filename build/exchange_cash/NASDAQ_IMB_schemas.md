# Nasdaq Auction Imbalance Data Schemas

Opening and Closing Auction Imbalance data for the Nasdaq Exchange




## NASDAQ_IMB

Database includes the following tick types:

* IND - Indicative pricing, e.g. indicative auction prices and imbalance



### NASDAQ_IMB - IND

Indicative pricing, e.g. indicative auction prices and imbalance

#### NASDAQ_IMB - IND Table Schema

| Field               | Data Type   | Description                                                                                                                                                                                                                            |
|---------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SYMBOL_NAME         | string      | Symbol Name (Exchange Symbol for Equities & ETFs, and Starting with Exchange Product Code for Derivative Markets followed by expiry and strike as appropriate)                                                                         |
| TIMESTAMP           | nsectime    | Event Timestamp (typically at a nano-second resolution)                                                                                                                                                                                |
| EXCH_TIME           | nsectime    | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp                                                                                                                      |
| REF_PRICE           | double      | Reference price according to which the auction price limits are set - usually the mid of the BBO, or the last sale price                                                                                                               |
| NEAR_PRICE          | double      | Theoretical auction price, taking into account orders in both the auction book and the continuous book                                                                                                                                 |
| FAR_PRICE           | double      | Theoretical auction price, taking into account only MOC/LOC orders (i.e. excluding orders in the continuous book)                                                                                                                      |
| SIZE                | long        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross                                       |
| IMB_SIDE            | string[1]   | Indicates if one side of the orderbook has excess executable orders during an auction phase.                                                                                                                                           |
| IMB_VOLUME          | long        | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE                                                                                                                                       |
| AUCTION_TYPE        | string[1]   | Type of auction from which an indicative auction price / auction imbalance originates.                                                                                                                                                 |
| PRICE_VARIATION_IND | string[1]   | > Indicates the difference between the indicative auction price (Near price) and the instrument’s reference price in the continuous book.                                                                                              |
| OMDSEQ              | uint        | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first. |
