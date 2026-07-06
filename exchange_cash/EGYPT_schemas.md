# Egyptian Exchange Schemas

The Egyptian Exchange facilitates trading in equities, bonds, securitized mortgage and asset-backed securities of Egyptian companies.

## EGYPT

Database includes the following tick types:


* MKT - Market phase / instrument status information


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### EGYPT - MKT

Market phase / instrument status information

### EGYPT - MKT Table Schema

| Field

 | Data Type

 | Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| MKT_PHASE

                     | string[4]

                                                                                                              | Indicates the instrument’s current market phase, as specified by the trading venue

                                                                                                                                                                |
| OMD_STATUS

                    | string[1]

                                                                                                              | Indicates an instrument’s current trading status. Values are normalized across all DBs.

                                                                                                                                                           |
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| TRADING_STATUS

                | string[4]

                                                                                                              | Indicates whether the instrument is subject to a halt or suspension

                                                                                                                                                                               |
### EGYPT - QTE

Best bid / offer quotes

### EGYPT - QTE Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
### EGYPT - STAT

Static data, e.g. ISIN, description, security type

### EGYPT - STAT Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BBG_TICKER

                    | string[30]

                                                                                                             | Bloomberg ticker symbol

                                                                                                                                                                                                                           |
| CURRENCY

                      | string[3]

                                                                                                              | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                   | string[20]

                                                                                                             | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| FIGI

                          | string[12]

                                                                                                             | Financial Instrument Global Identifier, identifying an individual instrument traded on a specific venue

                                                                                                                                           |
| ISIN

                          | string[12]

                                                                                                             | ISIN code

                                                                                                                                                                                                                                         |
| LOT_SIZE

                      | double

                                                                                                                 | All standard order sizes must be an integer multiple of the Lot Size

                                                                                                                                                                              |
| MIC

                           | string[4]

                                                                                                              | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                                  |
| NAME

                          | string[120]

                                                                                                            | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| OPERATING_MIC

                 | string[4]

                                                                                                              | Market Identifier Code (MIC, ISO 10383) of the exchange that operates the market on which the instrument is traded

                                                                                                                                |
| RTS_SYMBOL

                    | string[32]

                                                                                                             | Ticker symbol used by ICE Data Services

                                                                                                                                                                                                           |
| SEC_TYPE

                      | string[20]

                                                                                                             | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
| SEDOL

                         | string[7]

                                                                                                              | SEDOL code

                                                                                                                                                                                                                                        |
| TICK_SIZE

                     | string[50]

                                                                                                             | Tick size / minimum price increment. All order prices must be a multiple of the tick size.

                                                                                                                                                        |
| TICK_SIZE_TYPE

                | string[8]

                                                                                                              | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.

                                                                                                                                                              |
### EGYPT - TRD

Trades

### EGYPT - TRD Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DELETED_TIME

                  | msectime

                                                                                                               | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                  |
| EXCH_TIME

                     | nsectime

                                                                                                               | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRICE

                         | double

                                                                                                                 | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                         |
| SIZE

                          | long

                                                                                                                   | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| TICK_STATUS

                   | int

                                                                                                                    | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                      |
| TRADE_TYPE

                    | string[6]

                                                                                                              | Type of trade

                                                                                                                                                                                                                                     |
## EGYPT_BARS

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* MKT - Market phase / instrument status information


* QTE_1M - 1-minute quote bars

### EGYPT_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### EGYPT_BARS - DAY Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CLOSE

                         | double

                                                                                                                 | Closing price

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
| VOLUME

                        | long

                                                                                                                   | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### EGYPT_BARS - MKT

Market phase / instrument status information

### EGYPT_BARS - MKT Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MKT_PHASE

                     | string[4]

                                                                                                              | Indicates the instrument’s current market phase, as specified by the trading venue

                                                                                                                                                                |
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| OMD_STATUS

                    | string[64]

                                                                                                             | Indicates an instrument’s current trading status. Values are normalized across all DBs.

                                                                                                                                                           |
| TRADING_STATUS

                | string[4]

                                                                                                              | Indicates whether the instrument is subject to a halt or suspension

                                                                                                                                                                               |
### EGYPT_BARS - QTE_1M

1-minute quote bars

### EGYPT_BARS - QTE_1M Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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

