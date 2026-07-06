# National Stock Exchange of India - Equities Schemas

The NSE is India’s largest stock exchange offering trading in Indian company stocks and equity products.

## NSE_CASH

Database includes the following tick types:


* IDX - Index values


* PRL_ACTIVE - Shows all orders entered into the book, including aggressive orders that are matched immediately


* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)


* PRL_INACTIVE - Shows dormant / inactive orders (e.g. unelected stop orders) that are parked outside the main order book


* QTE - Best bid / offer quotes


* TRD - Trades

### NSE_CASH - IDX

Index values

### NSE_CASH - IDX Table Schema

| Field

 | Data Type

 | Description

 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| OMDSEQ

                        | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRICE

                         | double

                                                                                                                                     | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                         |
### NSE_CASH - PRL_ACTIVE

Shows all orders entered into the book, including aggressive orders that are matched immediately

### NSE_CASH - PRL_ACTIVE Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ALGO_TYPE

                     | string[1]

                                                                                                                                  | Type of algorithm / routing properties associated with an order

                                                                                                                                                                                   |
| BUY_SELL_FLAG

                 | int

                                                                                                                                        | Orderbook side (0 - Buy, 1 - Sell)

                                                                                                                                                                                                                |
| DELETED_TIME

                  | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                  |
| DISCLOSED_SIZE

                | int

                                                                                                                                        | Disclosed order quantity

                                                                                                                                                                                                                          |
| EXCH_TIME

                     | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| IOC_FLAG

                      | string[1]

                                                                                                                                  | Y - Immediate or Cancel (IOC) order, N - Not an IOC order

                                                                                                                                                                                         |
| MKT_ORDER_FLAG

                | string[1]

                                                                                                                                  | Y - Market order, N - Limit order

                                                                                                                                                                                                                 |
| OMD_PASSIVE_FLAG

              | string[1]

                                                                                                                                  | OMD Passive Flag

                                                                                                                                                                                                                                  |
| OMDSEQ

                        | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| ORDER_CAPACITY

                | string[1]

                                                                                                                                  | Indicates whether the participant that entered the order was acting in a Principal / Agency / Custodial capacity

                                                                                                                                  |
| ORDER_ID

                      | string[16]

                                                                                                                                 | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.

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

                          | int

                                                                                                                                        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| STOP_LOSS_FLAG

                | string[1]

                                                                                                                                  | Y - Stop order, N - Not a stop order

                                                                                                                                                                                                              |
| STOP_PRICE

                    | double

                                                                                                                                     | Stop price; price limit at which a dormant stop order is activated and injected into the active order book

                                                                                                                                        |
| TICK_STATUS

                   | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                      |
| TIME_PRIORITY

                 | long

                                                                                                                                       | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.

                                                                 |
### NSE_CASH - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

### NSE_CASH - PRL_FULL Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ALGO_TYPE

                     | string[1]

                                                                                                                                  | Type of algorithm / routing properties associated with an order

                                                                                                                                                                                   |
| BUY_SELL_FLAG

                 | int

                                                                                                                                        | Orderbook side (0 - Buy, 1 - Sell)

                                                                                                                                                                                                                |
| DELETED_TIME

                  | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                  |
| DISCLOSED_SIZE

                | int

                                                                                                                                        | Disclosed order quantity

                                                                                                                                                                                                                          |
| EXCH_TIME

                     | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| MKT_ORDER_FLAG

                | string[1]

                                                                                                                                  | Y - Market order, N - Limit order

                                                                                                                                                                                                                 |
| OMDSEQ

                        | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| ORDER_CAPACITY

                | string[1]

                                                                                                                                  | Indicates whether the participant that entered the order was acting in a Principal / Agency / Custodial capacity

                                                                                                                                  |
| ORDER_ID

                      | string[16]

                                                                                                                                 | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.

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

                          | int

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
### NSE_CASH - PRL_INACTIVE

Shows dormant / inactive orders (e.g. unelected stop orders) that are parked outside the main order book

### NSE_CASH - PRL_INACTIVE Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ALGO_TYPE

                     | string[1]

                                                                                                                                  | Type of algorithm / routing properties associated with an order

                                                                                                                                                                                   |
| BUY_SELL_FLAG

                 | int

                                                                                                                                        | Orderbook side (0 - Buy, 1 - Sell)

                                                                                                                                                                                                                |
| DELETED_TIME

                  | msectime

                                                                                                                                   | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                  |
| DISCLOSED_SIZE

                | int

                                                                                                                                        | Disclosed order quantity

                                                                                                                                                                                                                          |
| EXCH_TIME

                     | nsectime

                                                                                                                                   | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| IOC_FLAG

                      | string[1]

                                                                                                                                  | Y - Immediate or Cancel (IOC) order, N - Not an IOC order

                                                                                                                                                                                         |
| MKT_ORDER_FLAG

                | string[1]

                                                                                                                                  | Y - Market order, N - Limit order

                                                                                                                                                                                                                 |
| OMD_PASSIVE_FLAG

              | string[1]

                                                                                                                                  | OMD Passive Flag

                                                                                                                                                                                                                                  |
| OMDSEQ

                        | uint

                                                                                                                                       | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| ORDER_CAPACITY

                | string[1]

                                                                                                                                  | Indicates whether the participant that entered the order was acting in a Principal / Agency / Custodial capacity

                                                                                                                                  |
| ORDER_ID

                      | string[16]

                                                                                                                                 | Order identifier, uniquely identifying an order at any given point in time.   Uniqueness depends on the exchange - e.g. may be globally unique, or unique per trading day, or per instrument per trading day.

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

                          | int

                                                                                                                                        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| STOP_LOSS_FLAG

                | string[1]

                                                                                                                                  | Y - Stop order, N - Not a stop order

                                                                                                                                                                                                              |
| STOP_PRICE

                    | double

                                                                                                                                     | Stop price; price limit at which a dormant stop order is activated and injected into the active order book

                                                                                                                                        |
| TICK_STATUS

                   | int

                                                                                                                                        | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                      |
| TIME_PRIORITY

                 | long

                                                                                                                                       | Time priority of an order in the order queue.  If two standard orders on the same side have the same price, the one with the lower value of TIME_PRIORITY will be executed first.

                                                                 |
### NSE_CASH - QTE

Best bid / offer quotes

### NSE_CASH - QTE Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### NSE_CASH - TRD

Trades

### NSE_CASH - TRD Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AGGRESSOR_SIDE

                | string[1]

                                                                                                                                  | Indicates whether a trade resulted from an incoming buy or sell order.

                                                                                                                                                                            |
| BUY_ALGO_TYPE

                 | string[1]

                                                                                                                                  | Type of algorithm / routing properties associated with the order on the buy side of a trade

                                                                                                                                                       |
| BUY_ORDER_CAPACITY

            | string[1]

                                                                                                                                  | Indicates whether the buyer was acting in a Principal / Agency / Custodial capacity

                                                                                                                                                               |
| BUY_ORDER_ID

                  | string[16]

                                                                                                                                 | ID of the buy order involved in a trade

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
| SELL_ALGO_TYPE

                | string[1]

                                                                                                                                  | Type of algorithm / routing properties associated with the order on the sell side of a trade

                                                                                                                                                      |
| SELL_ORDER_CAPACITY

           | string[1]

                                                                                                                                  | Indicates whether the seller was acting in a Principal / Agency / Custodial capacity

                                                                                                                                                              |
| SELL_ORDER_ID

                 | string[16]

                                                                                                                                 | ID of the sell order involved in a trade

                                                                                                                                                                                                          |
| SIZE

                          | int

                                                                                                                                        | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| TRADE_ID

                      | string[20]

                                                                                                                                 | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                |
| TRADE_PERIOD

                  | string[1]

                                                                                                                                  | Market period during which a trade was executed.

                                                                                                                                                                                                  |
## NSE_CASH_BARS

Database includes the following tick types:


* QTE_1M - 1-minute quote bars


* TRD_1D - Daily trade bars


* TRD_1M - 1-minute trade bars


* VWAP_1H - 1-hour VWAP bars

### NSE_CASH_BARS - QTE_1M

1-minute quote bars

### NSE_CASH_BARS - QTE_1M Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### NSE_CASH_BARS - TRD_1D

Daily trade bars

### NSE_CASH_BARS - TRD_1D Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### NSE_CASH_BARS - TRD_1M

1-minute trade bars

### NSE_CASH_BARS - TRD_1M Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### NSE_CASH_BARS - VWAP_1H

1-hour VWAP bars

### NSE_CASH_BARS - VWAP_1H Table Schema

| Field

                         | Data Type

                                                                                                                                  | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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

