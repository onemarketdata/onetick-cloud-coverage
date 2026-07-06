# TSX Venture Exchange Schemas

The TSX Venture Exchange is a Canadian stock exchange for emerging companies operated by the TMX Group.

## TSXV

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* IND - Indicative pricing, e.g. indicative auction prices and imbalance


* MKT - Market phase / instrument status information


* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### TSXV - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### TSXV - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
### TSXV - IND

Indicative pricing, e.g. indicative auction prices and imbalance

### TSXV - IND Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AUCTION_TYPE

                      | string[1]

                                                                                                                                  | Type of auction from which an indicative auction price / auction imbalance originates.

                                                                                                                                                                        |
| EXCH_TIME

                         | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                             |
| FAR_PRICE

                         | double

                                                                                                                                     | Theoretical auction price, taking into account only MOC/LOC orders (i.e. excluding orders in the continuous book)

                                                                                                                                             |
| IMB_SIDE

                          | string[1]

                                                                                                                                  | Indicates if one side of the orderbook has excess executable orders during an auction phase.

                                                                                                                                                                  |
| IMB_VOLUME

                        | long

                                                                                                                                       | Size of an auction imbalance, i.e. the excess volume of orders on the side indicated by IMB_SIDE

                                                                                                                                                              |
| MKT_ORDER_IMB_SIDE

                | string[1]

                                                                                                                                  | Indicates if one side of the orderbook has excess market orders during an auction phase.

                                                                                                                                                                      |
| MKT_ORDER_IMB_VOLUME

              | long

                                                                                                                                       | Size of a market order imbalance, during an auction phase, i.e. the excess volume of market orders on the side indicated by IMB_SIDE

                                                                                                                          |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| PRICE

                             | double

                                                                                                                                     | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                                     |
| REF_PRICE

                         | double

                                                                                                                                     | Reference price according to which the auction price limits are set - usually the mid of the BBO, or the last sale price

                                                                                                                                      |
| SIZE

                              | long

                                                                                                                                       | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                              |
### TSXV - MKT

Market phase / instrument status information

### TSXV - MKT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MKT_PHASE

                         | string[4]

                                                                                                                                  | Indicates the instrument’s current market phase, as specified by the trading venue

                                                                                                                                                                            |
| OMD_STATUS

                        | string[64]

                                                                                                                                 | Indicates an instrument’s current trading status. Values are normalized across all DBs.

                                                                                                                                                                       |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
### TSXV - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

### TSXV - PRL_FULL Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BROKER_ID

                         | int

                                                                                                                                        | Identifies the market participant that entered an order / quote

                                                                                                                                                                                               |
| BUY_SELL_FLAG

                     | int

                                                                                                                                        | Orderbook side (0 - Buy, 1 - Sell)

                                                                                                                                                                                                                            |
| DELETED_TIME

                      | nsectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                              |
| EXCH_TIME

                         | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                             |
| FILL_SIZE

                         | int

                                                                                                                                        | Size filled in an order execution event

                                                                                                                                                                                                                       |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
| ORDER_ID

                          | string[24]

                                                                                                                                 | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.

                                                 |
| ORDER_TYPE

                        | string[1]

                                                                                                                                  | Type of order.

                                                                                                                                                                                                                                                |
| PRICE

                             | double

                                                                                                                                     | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                                     |
| RECORD_TYPE

                       | string[1]

                                                                                                                                  | Type of depth update.

                                                                                                                                                                                                                                         |
| SIZE

                              | long

                                                                                                                                       | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                              |
| TICK_STATUS

                       | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                                  |
| TIME_PRIORITY

                     | long

                                                                                                                                       | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.

                                                                             |
| TRADE_ID

                          | string[8]

                                                                                                                                  | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                            |
| UPDATE_TYPE

                       | string[1]

                                                                                                                                  | Type of update

                                                                                                                                                                                                                                                |
### TSXV - QTE

Best bid / offer quotes

### TSXV - QTE Table Schema

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
| EXCH_TIME

                         | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                             |
| OMDSEQ

                            | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

                        |
### TSXV - STAT

Static data, e.g. ISIN, description, security type

### TSXV - STAT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| MIC

                               | string[4]

                                                                                                                                  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                                              |
| NAME

                              | string[100]

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
| SEC_TYPE

                          | string[40]

                                                                                                                                 | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
### TSXV - TRD

Trades

### TSXV - TRD Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| DELETED_TIME

                      | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

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
| TICK_STATUS

                       | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                                  |
| TRADE_ID

                          | string[20]

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
## TSXV_BARS

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* MKT - Market phase / instrument status information


* QTE_1M - 1-minute quote bars


* TRD_1D - Daily trade bars


* TRD_1M - 1-minute trade bars


* VWAP_1H - 1-hour VWAP bars

### TSXV_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### TSXV_BARS - DAY Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### TSXV_BARS - MKT

Market phase / instrument status information

### TSXV_BARS - MKT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXCH_TIME

                         | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                             |
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
### TSXV_BARS - QTE_1M

1-minute quote bars

### TSXV_BARS - QTE_1M Table Schema

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
### TSXV_BARS - TRD_1D

Daily trade bars

### TSXV_BARS - TRD_1D Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUY_VOLUME

                        | long

                                                                                                                                       | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.

                                          |
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
| SELL_VOLUME

                       | long

                                                                                                                                       | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.

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
### TSXV_BARS - TRD_1M

1-minute trade bars

### TSXV_BARS - TRD_1M Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUY_VOLUME

                        | long

                                                                                                                                       | Traded volume originating from incoming buy orders.  Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.

                                          |
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
| SELL_VOLUME

                       | long

                                                                                                                                       | Traded volume originating from incoming sell orders. Excludes trades involving hidden orders, as well as off-book trades and auction trades, for the which the side of the aggressive order is undefined or unknown.

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
### TSXV_BARS - VWAP_1H

1-hour VWAP bars

### TSXV_BARS - VWAP_1H Table Schema

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
## TSXV_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type


* TRD_1D - Daily trade bars

### TSXV_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### TSXV_DAILY - DAY Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### TSXV_DAILY - STAT

Static data, e.g. ISIN, description, security type

### TSXV_DAILY - STAT Table Schema

| Field

                             | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| MIC

                               | string[4]

                                                                                                                                  | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                                              |
| NAME

                              | string[100]

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
| SEC_TYPE

                          | string[40]

                                                                                                                                 | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
### TSXV_DAILY - TRD_1D

Daily trade bars

### TSXV_DAILY - TRD_1D Table Schema

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

