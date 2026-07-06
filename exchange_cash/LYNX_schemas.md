# Lynx ATS Schemas

Lynx is an alternative trading system (ATS) or dark pool operated by Cboe Global Markets in Canada.

## LYNX

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* MKT - Market phase / instrument status information


* PRL_FULL - Full orderbook data, showing updates to each individual order (MBO)


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### LYNX - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### LYNX - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
### LYNX - MKT

Market phase / instrument status information

### LYNX - MKT Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### LYNX - PRL_FULL

Full orderbook data, showing updates to each individual order (MBO)

### LYNX - PRL_FULL Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| ORDER_ID

                      | string[20]

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
| TRADE_ID

                      | string[12]

                                                                                                             | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                |
| UPDATE_TYPE

                   | string[1]

                                                                                                              | Type of update

                                                                                                                                                                                                                                    |
### LYNX - QTE

Best bid / offer quotes

### LYNX - QTE Table Schema

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
| EXCH_TIME

                     | nsectime

                                                                                                               | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| OMDSEQ

                        | uint

                                                                                                                   | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
### LYNX - STAT

Static data, e.g. ISIN, description, security type

### LYNX - STAT Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### LYNX - TRD

Trades

### LYNX - TRD Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
## LYNX_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### LYNX_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### LYNX_DAILY - DAY Table Schema

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
### LYNX_DAILY - STAT

Static data, e.g. ISIN, description, security type

### LYNX_DAILY - STAT Table Schema

| Field

                         | Data Type

                                                                                                              | Description

                                                                                                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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

