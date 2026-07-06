# US Consolidated Equities (exc. OTC) Sample Schemas

A subset of symbols from the US SIP for trading between January 2,2024 and March 31, 2024

## US_COMP_SAMPLE

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* IND - Indicative pricing, e.g. indicative auction prices and imbalance


* LULD - Limit Up / Limit Down price levels


* MKT - Market phase / instrument status information


* NBBO - National Best Bid / Offer quotes


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### US_COMP_SAMPLE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### US_COMP_SAMPLE - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ | -------------------- | ----------------------- | ------------------------------- | ----------------------------- | ----------------------- | --------------- | ----------------------- | ----------------------- | ------------ | ----------------------------- | ----------------------------- | -------------------- | ----------------------- | ------------ | -------------- | -------------------- | ---------------- | ----------------------- | ---------------- | --------------- | ----------------------- | ----------------- | ------------- | ------------- | ------------------- | -------- | ---------------- | ---------- | --------------- | ------------- | ----------- | -------------- | ---------------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| CLOSE

                             | double

                                                                                                                                     | Closing price

                                                                                                                                                                                                                                                 |
| EXCHANGE

                          | string[4]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| HIGH

                              | double

                                                                                                                                     | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval

                                                                                                                                   |
| LOW

                               | double

                                                                                                                                     | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval

                                                                                                                                    |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| OPEN

                              | double

                                                                                                                                     | Open price for the current trading day

                                                                                                                                                                                                                        |
| PRICE_CLOSING_AUCTION

             | double

                                                                                                                                     | Price of the Closing Auction

                                                                                                                                                                                                                                  |
| PRICE_OPENING_AUCTION

             | double

                                                                                                                                     | Price of the Opening Auction

                                                                                                                                                                                                                                  |
| VOLUME

                            | long

                                                                                                                                       | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
| VOLUME_CLOSING_AUCTION

            | long

                                                                                                                                       | Volume of the Closing Auction

                                                                                                                                                                                                                                 |
| VOLUME_MAIN_SESSION

               | long

                                                                                                                                       | Volume of the Main Trading Session

                                                                                                                                                                                                                            |
| VOLUME_ODD_LOT

                    | long

                                                                                                                                       | Volume of the Odd Lot Trades

                                                                                                                                                                                                                                  |
| VOLUME_OFF_EXCHANGE

               | long

                                                                                                                                       | Volume of Off Exchange Trades

                                                                                                                                                                                                                                 |
| VOLUME_OPENING_AUCTION

            | long

                                                                                                                                       | Volume of the Opening Auction

                                                                                                                                                                                                                                 |
| VOLUME_POST_MARKET

                | long

                                                                                                                                       | Volume of the Post-Market Trading Session

                                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET

                 | long

                                                                                                                                       | Volume of the Pre-Market Trading Session

                                                                                                                                                                                                                      |
| VOLUME_ROUND_LOT

                  | long

                                                                                                                                       | Volume of Round Lot Trades

                                                                                                                                                                                                                                    |
| VWAP

                              | double

                                                                                                                                     | Volume-weighted average price

                                                                                                                                                                                                                                 |
### US_COMP_SAMPLE - IND

Indicative pricing, e.g. indicative auction prices and imbalance

### US_COMP_SAMPLE - IND Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXCHANGE

                          | string[1]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| IMB_SIDE

                          | string[1]

                                                                                                                                  | Indicates if one side of the orderbook has excess executable orders during an auction phase.

                                                                                                                                                                  |
| IMB_VOLUME

                        | long

                                                                                                                                       | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE

                                                                                                                                                              |
| IND_TYPE

                          | string[1]

                                                                                                                                  | Type of indicative price update

                                                                                                                                                                                                                               |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| OPENING_RANGE_HIGH

                | double

                                                                                                                                     | Upper end of the expected opening price range

                                                                                                                                                                                                                 |
| OPENING_RANGE_LOW

                 | double

                                                                                                                                     | Lower end of the expected opening price range

                                                                                                                                                                                                                 |
| PARTICIPANT_TIME

                  | nsectime

                                                                                                                                   | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed

                                                                                                                                           |
| SEQ_NUM

                           | long

                                                                                                                                       | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds

                                                                                                               |
### US_COMP_SAMPLE - LULD

Limit Up / Limit Down price levels

### US_COMP_SAMPLE - LULD Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| HIGH_LIMIT

                        | double

                                                                                                                                     | Upper trading limit / circuit breaker level

                                                                                                                                                                                                                   |
| LOW_LIMIT

                         | double

                                                                                                                                     | Lower trading limit / circuit breaker level

                                                                                                                                                                                                                   |
| LULD_IND

                          | string[2]

                                                                                                                                  | Type of Limit Up / Limit Down (LULD) price update

                                                                                                                                                                                                             |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| SEQ_NUM

                           | long

                                                                                                                                       | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds

                                                                                                               |
### US_COMP_SAMPLE - MKT

Market phase / instrument status information

### US_COMP_SAMPLE - MKT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXCHANGE

                          | string[1]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PARTICIPANT_TIME

                  | nsectime

                                                                                                                                   | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed

                                                                                                                                           |
| REASON_CODE

                       | string[6]

                                                                                                                                  | Reason for an instrument status update

                                                                                                                                                                                                                        |
| SEQ_NUM

                           | long

                                                                                                                                       | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds

                                                                                                               |
| SHORT_SALE_RESTRICTION

            | string[1]

                                                                                                                                  | Indicates whether short selling is permitted

                                                                                                                                                                                                                  |
| TRADING_STATUS

                    | string[1]

                                                                                                                                  | Indicates whether the instrument is subject to a halt or suspension

                                                                                                                                                                                           |
### US_COMP_SAMPLE - NBBO

National Best Bid / Offer quotes

### US_COMP_SAMPLE - NBBO Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_EXCHANGE

                      | string[2]

                                                                                                                                  | Exchange that set the best ask

                                                                                                                                                                                                                                |
| ASK_PRICE

                         | double

                                                                                                                                     | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                              |
| ASK_SIZE

                          | int

                                                                                                                                        | Best ask size

                                                                                                                                                                                                                                                 |
| ASK_SIZE_TOTAL

                    | int

                                                                                                                                        | Total size at the (national) best ask price across all participant markets

                                                                                                                                                                                    |
| BID_EXCHANGE

                      | string[2]

                                                                                                                                  | Exchange that set the best bid

                                                                                                                                                                                                                                |
| BID_PRICE

                         | double

                                                                                                                                     | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                                              |
| BID_SIZE

                          | int

                                                                                                                                        | Best bid size

                                                                                                                                                                                                                                                 |
| BID_SIZE_TOTAL

                    | int

                                                                                                                                        | Total size at the (national) best bid price across all participant markets

                                                                                                                                                                                    |
| IS_PRE_OPEN

                       | int

                                                                                                                                        | Indicates whether a quote originates from the period before (1) or after (0) the instrument has opened on the primary market

                                                                                                                                  |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
### US_COMP_SAMPLE - QTE

Best bid / offer quotes

### US_COMP_SAMPLE - QTE Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_PRICE

                         | double

                                                                                                                                     | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                              |
| ASK_SIZE

                          | long

                                                                                                                                       | Best ask size

                                                                                                                                                                                                                                                 |
| BID_PRICE

                         | double

                                                                                                                                     | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                                              |
| BID_SIZE

                          | long

                                                                                                                                       | Best bid size

                                                                                                                                                                                                                                                 |
| COND

                              | string[1]

                                                                                                                                  | Condition code

                                                                                                                                                                                                                                                |
| CORR

                              | string[1]

                                                                                                                                  | Type of trade correction / cancellation

                                                                                                                                                                                                                       |
| DELETED_TIME

                      | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                              |
| EXCHANGE

                          | string[1]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| FINRA_ADF_IND

                     | string[1]

                                                                                                                                  | Indicates whether the quote reflects the FINRA BBO

                                                                                                                                                                                                            |
| FINRA_ADF_MPID_IND

                | string[1]

                                                                                                                                  | Indicates whether a FINRA participant ID is available for a BBO quote [currently unused]

                                                                                                                                                                      |
| FINRA_ADF_TIME

                    | nsectime

                                                                                                                                   | Timestamp provided by a FINRA ADF

                                                                                                                                                                                                                             |
| FINRA_BBO_IND

                     | string[1]

                                                                                                                                  | Indicates whether the quote affects the FINRA BBO [currently unused]

                                                                                                                                                                                          |
| LULD_BBO_IND

                      | string[1]

                                                                                                                                  | Indicates whether the bid/ask crosses the upper / lower LULD price bands

                                                                                                                                                                                      |
| NBBO_IND

                          | string[1]

                                                                                                                                  | Indicates whether the quote affects the NBBO

                                                                                                                                                                                                                  |
| NBBO_LULD_IND

                     | string[1]

                                                                                                                                  | Indicates whether the NBBO crosses the upper / lower LULD price bands

                                                                                                                                                                                         |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PARTICIPANT_TIME

                  | nsectime

                                                                                                                                   | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed

                                                                                                                                           |
| RESTRICTION_IND

                   | string[1]

                                                                                                                                  | Indicates whether short selling is permitted

                                                                                                                                                                                                                  |
| RPI

                               | string[1]

                                                                                                                                  | Indicates the presence of Retail Price Improvement interest on bid and/or ask side

                                                                                                                                                                            |
| SECURITY_STATUS_IND

               | string[2]

                                                                                                                                  | Security status

                                                                                                                                                                                                                                               |
| SEQ_NUM

                           | long

                                                                                                                                       | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds

                                                                                                               |
| SIP_MSG_ID

                        | string[1]

                                                                                                                                  | Identifies messages generated by the SIP ( - Originates from an exchange, E - UTP, S - Consolidated Tape System)

                                                                                                                                              |
| SOURCE

                            | string[1]

                                                                                                                                  | Source from which an update originates

                                                                                                                                                                                                                        |
| TICK_STATUS

                       | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                                  |
| TICKER

                            | string[16]

                                                                                                                                 | Ticker symbol, as specified by the data source

                                                                                                                                                                                                                |
### US_COMP_SAMPLE - STAT

Static data, e.g. ISIN, description, security type

### US_COMP_SAMPLE - STAT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CONSOLIDATED_TAPE

                 | string[1]

                                                                                                                                  | Consolidated Tape on which a US security is published (A/B/C).

                                                                                                                                                                                                |
| LISTING_DATE

                      | string[8]

                                                                                                                                  | Date when the instrument was listed (YYYYMMDD)

                                                                                                                                                                                                                |
| LOT_SIZE

                          | double

                                                                                                                                     | All standard order sizes must be an integer multiple of the Lot Size

                                                                                                                                                                                          |
| NAME

                              | string[200]

                                                                                                                                | Description of the instrument

                                                                                                                                                                                                                                 |
| NYSE_INDUSTRY_CODE

                | string[4]

                                                                                                                                  | Industry classification, as defined by NYSE

                                                                                                                                                                                                                   |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PREV_SYMBOL

                       | string[16]

                                                                                                                                 | Previous ticker symbol, in the event of a symbol change

                                                                                                                                                                                                       |
| PRIMARY_MIC

                       | string[4]

                                                                                                                                  | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF

                                                                                                                                                      |
| SEC_TYPE

                          | string[30]

                                                                                                                                 | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
| SHARES_OUTSTANDING

                | long

                                                                                                                                       | Shares / quantity outstanding

                                                                                                                                                                                                                                 |
| SIP_SYMBOL

                        | string[16]

                                                                                                                                 | Ticker symbol used by the US Securities Information Processor (CTA / UTP)

                                                                                                                                                                                     |
| TEST_SYMBOL

                       | string[1]

                                                                                                                                  | Y - Test symbol, N - Not a test symbol

                                                                                                                                                                                                                        |
| TICK_PILOT_IND

                    | string[20]

                                                                                                                                 | Specifies any tick size pilot initiatives in which the instrument is participating

                                                                                                                                                                            |
### US_COMP_SAMPLE - TRD

Trades

### US_COMP_SAMPLE - TRD Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| COND

                              | string[4]

                                                                                                                                  | Condition code

                                                                                                                                                                                                                                                |
| CORR

                              | int

                                                                                                                                        | Type of trade correction / cancellation

                                                                                                                                                                                                                       |
| DELETED_TIME

                      | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                              |
| EXCHANGE

                          | string[1]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PARTICIPANT_TIME

                  | nsectime

                                                                                                                                   | Event timestamp (e.g. trade execution time), as provided by one of the participant exchanges in a consolidated feed

                                                                                                                                           |
| PRICE

                             | double

                                                                                                                                     | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                                     |
| SEQ_NUM

                           | long

                                                                                                                                       | Sequence number of the update, as specified by the exchange (for single exchange feeds) or the aggregator (e.g. CTA/UTP) for consolidated feeds

                                                                                                               |
| SIZE

                              | long

                                                                                                                                       | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                              |
| SOURCE

                            | string[1]

                                                                                                                                  | Source from which an update originates

                                                                                                                                                                                                                        |
| STOP_STOCK

                        | string[1]

                                                                                                                                  | Y - Stopped stock trade, N - Not a stopped stock trade,  - Not applicable

                                                                                                                                                                                     |
| TICK_STATUS

                       | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                                  |
| TICKER

                            | string[16]

                                                                                                                                 | Ticker symbol, as specified by the data source

                                                                                                                                                                                                                |
| TRADE_ID

                          | string[20]

                                                                                                                                 | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                            |
| TRF

                               | string[1]

                                                                                                                                  | Trade Reporting Facility used to report a trade (for trades reported to FINRA)

                                                                                                                                                                                |
| TRF_TIME

                          | nsectime

                                                                                                                                   | Time at which a trade was processed by the Trade Reporting Facility (for trades reported to FINRA)

                                                                                                                                                            |
| TTE

                               | string[1]

                                                                                                                                  | Indicates whether a trade is exempt from the Trade Through Rule (1 - Trade Through Exempt, 0 - No Trade Through Exemption)

                                                                                                                                    |
## US_COMP_SAMPLE_BARS

Database includes the following tick types:


* QTE_1M - 1-minute quote bars


* TRD_1D - Daily trade bars


* TRD_1M - 1-minute trade bars


* VWAP_1H - 1-hour VWAP bars

### US_COMP_SAMPLE_BARS - QTE_1M

1-minute quote bars

### US_COMP_SAMPLE_BARS - QTE_1M Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_PRICE_AT_HIGH_BID

             | double

                                                                                                                                     | Ask price of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.

                                                                                                                                               |
| ASK_SIZE_AT_HIGH_BID

              | long

                                                                                                                                       | Ask size of the quote that set HIGH_BID.  If there are multiple bid quotes at HIGH_BID, the first one is used.

                                                                                                                                                |
| BID_PRICE_AT_LOW_ASK

              | double

                                                                                                                                     | Bid price of the quote that set LOW_ASK. If there are multiple ask quotes at LOW_ASK, the first one is used.

                                                                                                                                                  |
| BID_SIZE_LOW_ASK

                  | long

                                                                                                                                       | Bid size of the quote that set LOW_ASK.  If there are multiple ask quotes at LOW_ASK, the first one is used.

                                                                                                                                                  |
| CLOUD_DB

                          | string[32]

                                                                                                                                 | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                                    |
| FIRST_ASK_PRICE

                   | double

                                                                                                                                     | Price of the first best ask update in the current bar interval

                                                                                                                                                                                                |
| FIRST_ASK_SIZE

                    | long

                                                                                                                                       | Size of the first best ask update in the current bar interval

                                                                                                                                                                                                 |
| FIRST_ASK_TIME

                    | nsectime

                                                                                                                                   | Time of the first best ask update in the current bar interval

                                                                                                                                                                                                 |
| FIRST_BID_PRICE

                   | double

                                                                                                                                     | Price of the first best bid update in the current bar interval

                                                                                                                                                                                                |
| FIRST_BID_SIZE

                    | long

                                                                                                                                       | Size of the first best bid update in the current bar interval

                                                                                                                                                                                                 |
| FIRST_BID_TIME

                    | nsectime

                                                                                                                                   | Time of the first best bid update in the current bar interval

                                                                                                                                                                                                 |
| HIGH_BID

                          | double

                                                                                                                                     | Highest bid price in the current bar interval

                                                                                                                                                                                                                 |
| HIGH_BID_SIZE

                     | long

                                                                                                                                       | Size of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.

                                                                                                                                                  |
| HIGH_BID_TIME

                     | nsectime

                                                                                                                                   | Time of the bid quote that set HIGH_BID.  If there are multiple quotes at that price, the first one is used.

                                                                                                                                                  |
| LAST_ASK_PRICE

                    | double

                                                                                                                                     | Price of the last best ask update in the current bar interval

                                                                                                                                                                                                 |
| LAST_ASK_SIZE

                     | long

                                                                                                                                       | Size of the last best ask update in the current bar interval

                                                                                                                                                                                                  |
| LAST_ASK_TIME

                     | nsectime

                                                                                                                                   | Time of the last best ask update in the current bar interval

                                                                                                                                                                                                  |
| LAST_BID_PRICE

                    | double

                                                                                                                                     | Price of the last best bid update in the current bar interval

                                                                                                                                                                                                 |
| LAST_BID_SIZE

                     | long

                                                                                                                                       | Size of the last best bid update in the current bar interval

                                                                                                                                                                                                  |
| LAST_BID_TIME

                     | nsectime

                                                                                                                                   | Time of the last best bid update in the current bar interval

                                                                                                                                                                                                  |
| LOW_ASK

                           | double

                                                                                                                                     | Lowest ask price in the current bar interval

                                                                                                                                                                                                                  |
| LOW_ASK_SIZE

                      | long

                                                                                                                                       | Size of the ask quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.

                                                                                                                                                   |
| LOW_ASK_TIME

                      | nsectime

                                                                                                                                   | Time of the bid quote that set LOW_ASK.  If there are multiple quotes at that price, the first one is used.

                                                                                                                                                   |
| MID_LAST

                          | double

                                                                                                                                     | Midpoint of the last best bid/ask in the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]

                                                                                                                            |
| MID_MEDIAN

                        | double

                                                                                                                                     | Median of the midpoint of the best bid/ask quotes over the current bar interval. [Note: One-sided or empty quotes are excluded from the calculation]

                                                                                                          |
| MID_TWAP

                          | double

                                                                                                                                     | Time-weighted average of the midpoint of the best bid/ask over the current bar interval.  [Note: One-sided or empty quotes are excluded from the calculation]

                                                                                                 |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| QUOTE_CURRENCY

                    | string[3]

                                                                                                                                  | Currency in which a quote price is expressed.

                                                                                                                                                                                                                 |
| QUOTE_TICK_COUNT

                  | long

                                                                                                                                       | Number of BBO quotes in the current bar interval

                                                                                                                                                                                                              |
| SPREAD_LAST

                       | double

                                                                                                                                     | Last value of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]

                                                   |
| SPREAD_MAX

                        | double

                                                                                                                                     | Widest bid/ask spread, i.e. the highest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]

               |
| SPREAD_MEDIAN

                     | double

                                                                                                                                     | Median value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]

                                                |
| SPREAD_MIN

                        | double

                                                                                                                                     | Narrowest bid/ask spread, i.e. the lowest value of (best ask price - best bid price) over the current bar interval.   [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]

             |
| SPREAD_TWAP

                       | double

                                                                                                                                     | Time-weighted average of (best ask price - best bid price) over the current bar interval.  [Note: May be zero or negative if the book was locked/crossed. One-sided or empty quotes are excluded from the calculation]

                                        |
### US_COMP_SAMPLE_BARS - TRD_1D

Daily trade bars

### US_COMP_SAMPLE_BARS - TRD_1D Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLOUD_DB

                          | string[32]

                                                                                                                                 | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                                    |
| FIRST

                             | double

                                                                                                                                     | Price of the first eligible trade in the current bar interval

                                                                                                                                                                                                 |
| FIRST_SIZE

                        | long

                                                                                                                                       | Size of the first eligible trade in the current bar interval

                                                                                                                                                                                                  |
| FIRST_TIME

                        | nsectime

                                                                                                                                   | Timestamp of the first eligible trade in the current bar interval

                                                                                                                                                                                             |
| HIGH

                              | double

                                                                                                                                     | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval

                                                                                                                                   |
| HIGH_SIZE

                         | long

                                                                                                                                       | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                           |
| HIGH_TIME

                         | nsectime

                                                                                                                                   | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                      |
| LAST

                              | double

                                                                                                                                     | Price of the last eligible trade in the current bar interval

                                                                                                                                                                                                  |
| LAST_SIZE

                         | long

                                                                                                                                       | Size of the last eligible trade in the current bar interval

                                                                                                                                                                                                   |
| LAST_TIME

                         | nsectime

                                                                                                                                   | Timestamp of the last eligible trade in the current bar interval

                                                                                                                                                                                              |
| LOW

                               | double

                                                                                                                                     | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval

                                                                                                                                    |
| LOW_SIZE

                          | long

                                                                                                                                       | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                            |
| LOW_TIME

                          | nsectime

                                                                                                                                   | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                       |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| TRADE_CURRENCY

                    | string[3]

                                                                                                                                  | Currency in which a trade was executed.

                                                                                                                                                                                                                       |
| TRADE_TICK_COUNT

                  | long

                                                                                                                                       | Number of eligible trades in the current bar interval

                                                                                                                                                                                                         |
| TWAP

                              | double

                                                                                                                                     | TIme-weighted average price

                                                                                                                                                                                                                                   |
| VOLUME

                            | long

                                                                                                                                       | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
| VWAP

                              | double

                                                                                                                                     | Volume-weighted average price

                                                                                                                                                                                                                                 |
### US_COMP_SAMPLE_BARS - TRD_1M

1-minute trade bars

### US_COMP_SAMPLE_BARS - TRD_1M Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLOUD_DB

                          | string[32]

                                                                                                                                 | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                                    |
| FIRST

                             | double

                                                                                                                                     | Price of the first eligible trade in the current bar interval

                                                                                                                                                                                                 |
| FIRST_SIZE

                        | long

                                                                                                                                       | Size of the first eligible trade in the current bar interval

                                                                                                                                                                                                  |
| FIRST_TIME

                        | nsectime

                                                                                                                                   | Timestamp of the first eligible trade in the current bar interval

                                                                                                                                                                                             |
| HIGH

                              | double

                                                                                                                                     | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval

                                                                                                                                   |
| HIGH_SIZE

                         | long

                                                                                                                                       | Size of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                           |
| HIGH_TIME

                         | nsectime

                                                                                                                                   | Timestamp of the highest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                      |
| LAST

                              | double

                                                                                                                                     | Price of the last eligible trade in the current bar interval

                                                                                                                                                                                                  |
| LAST_SIZE

                         | long

                                                                                                                                       | Size of the last eligible trade in the current bar interval

                                                                                                                                                                                                   |
| LAST_TIME

                         | nsectime

                                                                                                                                   | Timestamp of the last eligible trade in the current bar interval

                                                                                                                                                                                              |
| LOW

                               | double

                                                                                                                                     | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval

                                                                                                                                    |
| LOW_SIZE

                          | long

                                                                                                                                       | Size of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                            |
| LOW_TIME

                          | nsectime

                                                                                                                                   | Timestamp of the lowest-priced eligible trade in the current bar interval.  If there are multiple eligible trades at that price, the first one is used.

                                                                                                       |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| TRADE_CURRENCY

                    | string[3]

                                                                                                                                  | Currency in which a trade was executed.

                                                                                                                                                                                                                       |
| TRADE_TICK_COUNT

                  | long

                                                                                                                                       | Number of eligible trades in the current bar interval

                                                                                                                                                                                                         |
| TWAP

                              | double

                                                                                                                                     | TIme-weighted average price

                                                                                                                                                                                                                                   |
| VOLUME

                            | long

                                                                                                                                       | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
| VWAP

                              | double

                                                                                                                                     | Volume-weighted average price

                                                                                                                                                                                                                                 |
### US_COMP_SAMPLE_BARS - VWAP_1H

1-hour VWAP bars

### US_COMP_SAMPLE_BARS - VWAP_1H Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLOUD_DB

                          | string[32]

                                                                                                                                 | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                                    |
| CURRENCY

                          | string[64]

                                                                                                                                 | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                               |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| TWAP

                              | double

                                                                                                                                     | TIme-weighted average price

                                                                                                                                                                                                                                   |
| VOLUME

                            | double

                                                                                                                                     | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
| VWAP

                              | double

                                                                                                                                     | Volume-weighted average price

                                                                                                                                                                                                                                 |
## US_COMP_SAMPLE_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### US_COMP_SAMPLE_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### US_COMP_SAMPLE_DAILY - DAY Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLOSE

                             | double

                                                                                                                                     | Closing price

                                                                                                                                                                                                                                                 |
| EXCHANGE

                          | string[4]

                                                                                                                                  | Exchange from which the update originates

                                                                                                                                                                                                                     |
| HIGH

                              | double

                                                                                                                                     | DAY: High price for the current trading day  TRD_1M: Price of the highest-priced eligible trade in the current bar interval

                                                                                                                                   |
| LOW

                               | double

                                                                                                                                     | DAY: Low price for the current trading day.  TRD_1M: Price of the lowest-priced eligible trade in the current bar interval

                                                                                                                                    |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| OPEN

                              | double

                                                                                                                                     | Open price for the current trading day

                                                                                                                                                                                                                        |
| PRICE_CLOSING_AUCTION

             | double

                                                                                                                                     | Price of the Closing Auction

                                                                                                                                                                                                                                  |
| PRICE_OPENING_AUCTION

             | double

                                                                                                                                     | Price of the Opening Auction

                                                                                                                                                                                                                                  |
| VOLUME

                            | long

                                                                                                                                       | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
| VOLUME_CLOSING_AUCTION

            | long

                                                                                                                                       | Volume of the Closing Auction

                                                                                                                                                                                                                                 |
| VOLUME_MAIN_SESSION

               | long

                                                                                                                                       | Volume of the Main Trading Session

                                                                                                                                                                                                                            |
| VOLUME_ODD_LOT

                    | long

                                                                                                                                       | Volume of the Odd Lot Trades

                                                                                                                                                                                                                                  |
| VOLUME_OFF_EXCHANGE

               | long

                                                                                                                                       | Volume of Off Exchange Trades

                                                                                                                                                                                                                                 |
| VOLUME_OPENING_AUCTION

            | long

                                                                                                                                       | Volume of the Opening Auction

                                                                                                                                                                                                                                 |
| VOLUME_POST_MARKET

                | long

                                                                                                                                       | Volume of the Post-Market Trading Session

                                                                                                                                                                                                                     |
| VOLUME_PRE_MARKET

                 | long

                                                                                                                                       | Volume of the Pre-Market Trading Session

                                                                                                                                                                                                                      |
| VOLUME_ROUND_LOT

                  | long

                                                                                                                                       | Volume of Round Lot Trades

                                                                                                                                                                                                                                    |
| VWAP

                              | double

                                                                                                                                     | Volume-weighted average price

                                                                                                                                                                                                                                 |
### US_COMP_SAMPLE_DAILY - STAT

Static data, e.g. ISIN, description, security type

### US_COMP_SAMPLE_DAILY - STAT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CONSOLIDATED_TAPE

                 | string[1]

                                                                                                                                  | Consolidated Tape on which a US security is published (A/B/C).

                                                                                                                                                                                                |
| LISTING_DATE

                      | string[8]

                                                                                                                                  | Date when the instrument was listed (YYYYMMDD)

                                                                                                                                                                                                                |
| LOT_SIZE

                          | double

                                                                                                                                     | All standard order sizes must be an integer multiple of the Lot Size

                                                                                                                                                                                          |
| NAME

                              | string[200]

                                                                                                                                | Description of the instrument

                                                                                                                                                                                                                                 |
| NYSE_INDUSTRY_CODE

                | string[4]

                                                                                                                                  | Industry classification, as defined by NYSE

                                                                                                                                                                                                                   |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PREV_SYMBOL

                       | string[16]

                                                                                                                                 | Previous ticker symbol, in the event of a symbol change

                                                                                                                                                                                                       |
| PRIMARY_MIC

                       | string[4]

                                                                                                                                  | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF

                                                                                                                                                      |
| SEC_TYPE

                          | string[30]

                                                                                                                                 | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
| SHARES_OUTSTANDING

                | long

                                                                                                                                       | Shares / quantity outstanding

                                                                                                                                                                                                                                 |
| SIP_SYMBOL

                        | string[16]

                                                                                                                                 | Ticker symbol used by the US Securities Information Processor (CTA / UTP)

                                                                                                                                                                                     |
| TEST_SYMBOL

                       | string[1]

                                                                                                                                  | Y - Test symbol, N - Not a test symbol

                                                                                                                                                                                                                        |
| TICK_PILOT_IND

                    | string[20]

                                                                                                                                 | Specifies any tick size pilot initiatives in which the instrument is participating

