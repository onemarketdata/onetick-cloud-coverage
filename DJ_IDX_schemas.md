# Dow Jones Indices Schemas

Dow Jones Indices is a provider of global equity indices like the Dow Jones Industrial Average, tracking various markets and sectors across different asset classes and geographies.

## DJ_IDX

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* IDX - Index values


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type

### DJ_IDX - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### DJ_IDX - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| SETTLEMENT_INDEX

            | double

                                                                                                                       | Index value used to determine settlement prices for related derivatives contracts

                                                                                                                                                                 |
| VOLUME

                      | long

                                                                                                                         | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### DJ_IDX - IDX

Index values

### DJ_IDX - IDX Table Schema

| Field

                       | Data Type

                                                                                                                    | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OMDSEQ

                      | uint

                                                                                                                         | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRICE

                       | double

                                                                                                                       | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                         |
| VOLUME

                      | long

                                                                                                                         | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
| YIELD

                       | double

                                                                                                                       | Yield to maturity, expressed as a percentage

                                                                                                                                                                                                      |
### DJ_IDX - QTE

Best bid / offer quotes

### DJ_IDX - QTE Table Schema

| Field

                       | Data Type

                                                                                                                    | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_PRICE

                   | double

                                                                                                                       | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| BID_PRICE

                   | double

                                                                                                                       | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| OMDSEQ

                      | uint

                                                                                                                         | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
### DJ_IDX - STAT

Static data, e.g. ISIN, description, security type

### DJ_IDX - STAT Table Schema

| Field

                       | Data Type

                                                                                                                    | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CURRENCY

                    | string[3]

                                                                                                                    | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                 | string[20]

                                                                                                                   | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| NAME

                        | string[120]

                                                                                                                  | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                      | uint

                                                                                                                         | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| SEC_TYPE

                    | string[40]

                                                                                                                   | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
## DJ_IDX_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### DJ_IDX_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### DJ_IDX_DAILY - DAY Table Schema

| Field

                       | Data Type

                                                                                                                    | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| SETTLEMENT_INDEX

            | double

                                                                                                                       | Index value used to determine settlement prices for related derivatives contracts

                                                                                                                                                                 |
| VOLUME

                      | long

                                                                                                                         | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### DJ_IDX_DAILY - STAT

Static data, e.g. ISIN, description, security type

### DJ_IDX_DAILY - STAT Table Schema

| Field

                       | Data Type

                                                                                                                    | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CURRENCY

                    | string[3]

                                                                                                                    | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_SYMBOL

                 | string[20]

                                                                                                                   | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| NAME

                        | string[120]

                                                                                                                  | Description of the instrument

                                                                                                                                                                                                                     |
| OMDSEQ

                      | uint

                                                                                                                         | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| SEC_TYPE

                    | string[40]

                                                                                                                   | Security type, e.g. Equity, ETF, Future

