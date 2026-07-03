# Metropolitan Stock Exchange of India Schemas

The Metropolitan Stock Exchange of India (MSEI) offers trading in equities, bonds, ETFs, and derivatives.

## MSEI

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### MSEI - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### MSEI - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| OPEN_INT

                    | double

                                                                                                                            | Open interest for futures / options

                                                                                                                                                                                                                           |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                              |
| VOLUME

                      | long

                                                                                                                              | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
### MSEI - STAT

Static data, e.g. ISIN, description, security type

### MSEI - STAT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CONTRACT_SIZE

               | double

                                                                                                                            | Indicates a derivative’s underlying quantity

                                                                                                                                                                                                                  |
| CURRENCY

                    | string[3]

                                                                                                                         | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                               |
| EXPIRATION_DATE

             | string[8]

                                                                                                                         | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                                                     |
| MIC

                         | string[4]

                                                                                                                         | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                                              |
| NAME

                        | string[150]

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
| PRODUCT_CODE

                | string[10]

                                                                                                                        | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.

                    |
| RTS_SYMBOL

                  | string[32]

                                                                                                                        | Ticker symbol used by ICE Data Services

                                                                                                                                                                                                                       |
| SEC_TYPE

                    | string[20]

                                                                                                                        | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
| STRATEGY_TYPE

               | string[30]

                                                                                                                        | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly

                                                                                                                                                                                            |
| TICK_SIZE

                   | string[50]

                                                                                                                        | Tick size / minimum price increment. All order prices must be a multiple of the tick size.

                                                                                                                                                                    |
| TICK_SIZE_TYPE

              | string[8]

                                                                                                                         | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.

                                                                                                                                                                          |
| TICK_VALUE

                  | double

                                                                                                                            | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.

                                                                                                                                                           |
## MSEI_BARS

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest

### MSEI_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### MSEI_BARS - DAY Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OPEN_INT

                    | double

                                                                                                                            | Open interest for futures / options

                                                                                                                                                                                                                           |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                              |
| VOLUME

                      | long

                                                                                                                              | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
## MSEI_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### MSEI_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### MSEI_DAILY - DAY Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OPEN_INT

                    | double

                                                                                                                            | Open interest for futures / options

                                                                                                                                                                                                                           |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                              |
| VOLUME

                      | long

                                                                                                                              | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                             |
### MSEI_DAILY - STAT

Static data, e.g. ISIN, description, security type

### MSEI_DAILY - STAT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CONTRACT_SIZE

               | double

                                                                                                                            | Indicates a derivative’s underlying quantity

                                                                                                                                                                                                                  |
| CURRENCY

                    | string[3]

                                                                                                                         | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                               |
| EXPIRATION_DATE

             | string[8]

                                                                                                                         | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                                                     |
| MIC

                         | string[4]

                                                                                                                         | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                                              |
| NAME

                        | string[150]

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
| PRODUCT_CODE

                | string[10]

                                                                                                                        | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.

                    |
| RTS_SYMBOL

                  | string[32]

                                                                                                                        | Ticker symbol used by ICE Data Services

                                                                                                                                                                                                                       |
| SEC_TYPE

                    | string[20]

                                                                                                                        | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                                       |
| STRATEGY_TYPE

               | string[30]

                                                                                                                        | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly

                                                                                                                                                                                            |
| TICK_SIZE

                   | string[50]

                                                                                                                        | Tick size / minimum price increment. All order prices must be a multiple of the tick size.

                                                                                                                                                                    |
| TICK_SIZE_TYPE

              | string[8]

                                                                                                                         | Indicates the type of tick size carried by TICK_SIZE. Values are Static or Variable.

                                                                                                                                                                          |
| TICK_VALUE

                  | double

                                                                                                                            | Tick value, i.e. the profit / loss per contract resulting from a price movement equal to TICK_SIZE.

