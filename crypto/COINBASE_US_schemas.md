# Coinbase - US Exchange Schemas

Coinbase is the largest US-based cryptocurrency exchange, founded in 2012 by Brian Armstrong and Fred Ehrsam to facilitate Bitcoin trading. Headquartered in the US, it is a publicly traded company (NASDAQ: COIN) known as a major, regulated spot exchange with over 100 million users. It provides secure custodial services and trading for various digital assets.

## COINBASE_US

Database includes the following tick types:


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### COINBASE_US - QTE

Best bid / offer quotes

### COINBASE_US - QTE Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ASK_PRICE

                   | double

                                                                                                              | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| ASK_SIZE

                    | double

                                                                                                              | Best ask size

                                                                                                                                                                                                                                     |
| BID_PRICE

                   | double

                                                                                                              | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| BID_SIZE

                    | double

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
| QUOTE_VENUE

                 | string[12]

                                                                                                          | Venue (MIC) from which a quote originates

                                                                                                                                                                                                         |
### COINBASE_US - STAT

Static data, e.g. ISIN, description, security type

### COINBASE_US - STAT Table Schema

| Field

                       | Data Type

                                                                                                           | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CURRENCY

                    | string[12]

                                                                                                          | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                 | string[32]

                                                                                                          | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| EXPIRATION_DATE

             | string[8]

                                                                                                           | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                                         |
| NAME

                        | string[100]

                                                                                                         | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                      | uint

                                                                                                                | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| SEC_SUBTYPE

                 | string[40]

                                                                                                          | Security subtype

                                                                                                                                                                                                                                  |
| SEC_TYPE

                    | string[40]

                                                                                                          | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
### COINBASE_US - TRD

Trades

### COINBASE_US - TRD Table Schema

| Field

                       | Data Type

                                                                                                           | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AGGRESSOR_SIDE

              | string[1]

                                                                                                           | Indicates whether a trade resulted from an incoming buy or sell order.

                                                                                                                                                                            |
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

                        | double

                                                                                                              | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| TICK_STATUS

                 | int

                                                                                                                 | Internal OneTick field. Always 0 unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                      |
| TRADE_ID

                    | string[40]

                                                                                                          | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                |
| TRADE_VENUE

                 | string[12]

                                                                                                          | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.

