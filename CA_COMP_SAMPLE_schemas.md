# Canadian Consolidated Market Sample Schemas

A subset of symbols from all Canadian venues, between January 2,2024 and March 31, 2024

## CA_COMP_SAMPLE

Database includes the following tick types:


* NBBO - National Best Bid / Offer quotes


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### CA_COMP_SAMPLE - NBBO

National Best Bid / Offer quotes

### CA_COMP_SAMPLE - NBBO Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ASK_EXCHANGE

                | string[4]

                                                                                                              | Exchange that set the best ask

                                                                                                                                                                                                                    |
| ASK_PRICE

                   | double

                                                                                                                 | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| ASK_SIZE

                    | long

                                                                                                                   | Best ask size

                                                                                                                                                                                                                                     |
| BID_EXCHANGE

                | string[4]

                                                                                                              | Exchange that set the best bid

                                                                                                                                                                                                                    |
| BID_PRICE

                   | double

                                                                                                                 | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| BID_SIZE

                    | long

                                                                                                                   | Best bid size

                                                                                                                                                                                                                                     |
| EXCH_TIME

                   | nsectime

                                                                                                               | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| OMDSEQ

                      | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
### CA_COMP_SAMPLE - QTE

Best bid / offer quotes

### CA_COMP_SAMPLE - QTE Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| CLOUD_DB

                    | string[16]

                                                                                                             | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                        |
| EXCH_TIME

                   | nsectime

                                                                                                               | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| OMD_STATUS

                  | string[1]

                                                                                                              | Indicates an instrument’s current trading status. Values are normalized across all DBs.

                                                                                                                                                           |
| OMDSEQ

                      | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| QUOTE_VENUE

                 | string[4]

                                                                                                              | Venue (MIC) from which a quote originates

                                                                                                                                                                                                         |
### CA_COMP_SAMPLE - STAT

Static data, e.g. ISIN, description, security type

### CA_COMP_SAMPLE - STAT Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CURRENCY

                    | string[3]

                                                                                                              | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                 | string[20]

                                                                                                             | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| ISIN

                        | string[12]

                                                                                                             | ISIN code

                                                                                                                                                                                                                                         |
| LOT_SIZE

                    | double

                                                                                                                 | All standard order sizes must be an integer multiple of the Lot Size

                                                                                                                                                                              |
| NAME

                        | string[100]

                                                                                                            | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                      | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRIMARY_MIC

                 | string[4]

                                                                                                              | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF

                                                                                                                                          |
| SEC_TYPE

                    | string[40]

                                                                                                             | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
### CA_COMP_SAMPLE - TRD

Trades

### CA_COMP_SAMPLE - TRD Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BOOK_TYPE

                   | string[1]

                                                                                                              | Type of order book or trading mechanism through which a trade was executed.

                                                                                                                                                                       |
| BUYER

                       | string[4]

                                                                                                              | ID of the market participant on the buy side of a trade

                                                                                                                                                                                           |
| BYPASS

                      | string[1]

                                                                                                              | Identifies whether the trade resulted from a Bypass order

                                                                                                                                                                                         |
| CLOUD_DB

                    | string[16]

                                                                                                             | In composite DBs: Identifies the source database for each tick.  In bars DBs: Identifies the database containing the tick data used to calculate the bars.

                                                                                        |
| EXCH_TIME

                   | nsectime

                                                                                                               | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| ODD_LOT

                     | string[1]

                                                                                                              | Indicates whether a trade was an odd lot

                                                                                                                                                                                                          |
| OMDSEQ

                      | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRICE

                       | double

                                                                                                                 | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                         |
| SELLER

                      | string[4]

                                                                                                              | ID of the market participant on the sell side of a trade

                                                                                                                                                                                          |
| SIZE

                        | long

                                                                                                                   | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| SPECIAL_TERMS

               | string[2]

                                                                                                              | Indicates any non-standard settlement / execution terms associated with a trade

                                                                                                                                                                   |
| TRADE_ID

                    | string[24]

                                                                                                             | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                |
| TRADE_PERIOD

                | string[1]

                                                                                                              | Market period during which a trade was executed.

                                                                                                                                                                                                  |
| TRADE_TYPE

                  | string[8]

                                                                                                              | Type of trade

                                                                                                                                                                                                                                     |
| TRADE_VENUE

                 | string[4]

                                                                                                              | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.

                                                                                    |
## CA_COMP_SAMPLE_BARS

Database includes the following tick types:


* QTE_1M - 1-minute quote bars


* TRD_1D - Daily trade bars


* TRD_1M - 1-minute trade bars


* VWAP_1H - 1-hour VWAP bars

### CA_COMP_SAMPLE_BARS - QTE_1M

1-minute quote bars

### CA_COMP_SAMPLE_BARS - QTE_1M Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### CA_COMP_SAMPLE_BARS - TRD_1D

Daily trade bars

### CA_COMP_SAMPLE_BARS - TRD_1D Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### CA_COMP_SAMPLE_BARS - TRD_1M

1-minute trade bars

### CA_COMP_SAMPLE_BARS - TRD_1M Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### CA_COMP_SAMPLE_BARS - VWAP_1H

1-hour VWAP bars

### CA_COMP_SAMPLE_BARS - VWAP_1H Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
## CA_COMP_SAMPLE_DAILY

Database includes the following tick types:


* STAT - Static data, e.g. ISIN, description, security type

### CA_COMP_SAMPLE_DAILY - STAT

Static data, e.g. ISIN, description, security type

### CA_COMP_SAMPLE_DAILY - STAT Table Schema

| Field

                       | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CURRENCY

                    | string[3]

                                                                                                              | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                 | string[20]

                                                                                                             | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| ISIN

                        | string[12]

                                                                                                             | ISIN code

                                                                                                                                                                                                                                         |
| LOT_SIZE

                    | double

                                                                                                                 | All standard order sizes must be an integer multiple of the Lot Size

                                                                                                                                                                              |
| NAME

                        | string[100]

                                                                                                            | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                      | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRIMARY_MIC

                 | string[4]

                                                                                                              | MIC of the instrument’s primary listing market, or the reference market for instruments traded on an MTF

                                                                                                                                          |
| SEC_TYPE

                    | string[40]

                                                                                                             | Security type, e.g. Equity, ETF, Future

