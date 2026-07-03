# ARCA Imbalance Data Schemas

Opening and Closing Auction Imbalance data for the ARCA Exchange

## ARCA_IMB

Database includes the following tick types:


* IND - Indicative pricing, e.g. indicative auction prices and imbalance

### ARCA_IMB - IND

Indicative pricing, e.g. indicative auction prices and imbalance

### ARCA_IMB - IND Table Schema

| Field

 | Data Type

 | Description

 |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| AUCTION_TYPE

           | string[1]

                                                                                                           | Type of auction from which an indicative auction price / auction imbalance originates.

                                                                                                                                                            |
| CLEARING_PRICE

         | double

                                                                                                              | Price at which the order imbalance would be reduced to 0, disregarding auction price limits.  Indicates how far the market would have to move to negate the auction imbalance.

                                                                    |
| CLEARING_PRICE_AUCTION_BOOK

 | double

                                                                                                              | Price at which the imbalance in the auction book (i.e. excluding orders in the continuous book) would be reduced to 0, disregarding auction price limits

                                                                                          |
| COND

                        | string[1]

                                                                                                           | Condition code

                                                                                                                                                                                                                                    |
| EXCH_TIME

                   | nsectime

                                                                                                            | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| IMB_SIDE

                    | string[1]

                                                                                                           | Indicates if one side of the orderbook has excess executable orders during an auction phase.

                                                                                                                                                      |
| IMB_VOLUME

                  | long

                                                                                                                | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE

                                                                                                                                                  |
| OMDSEQ

                      | uint

                                                                                                                | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| REF_PRICE

                   | double

                                                                                                              | Reference price according to which the auction price limits are set - usually the mid of the BBO, or the last sale price

                                                                                                                          |
| SIZE

                        | long

                                                                                                                | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| SSR_FILING_PRICE

            | double

                                                                                                              | Price at which short selling orders will participate in an auction (if higher than their limit price), for securities subject to a short selling restriction

                                                                                      |
| UNPAIRED_SIDE

               | string[1]

                                                                                                           | During a closing auction on NYSE, indicates if one side of the orderbook has excess executable orders at the imbalance reference price.

                                                                                                           |
| UNPAIRED_VOLUME

             | long

                                                                                                                | For NYSE closing auctions, indicates the volume of excess orders on the side of the imbalance that are priced at or better than the imbalance reference price.

