# Abaxx Exchange Schemas

Abaxx Exchange introduces centrally cleared, physically delivered futures contracts and derivatives to provide better price signals, improved risk management capabilities and an enhanced network for energy, metals and environmental markets.

## ABAXX

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* MKT - Market phase / instrument status information


* QTE - Best bid / offer quotes


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### ABAXX - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### ABAXX - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------- | -------------- | ----------- | ---------- | ---------- | -------- |  |  |  |  |  |  |
| OMDSEQ

                | uint

           | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

 |
| SETTLE_DATE

           | string[8]

      | Trading date to which the settlement price relates (YYYYMMDD)

                                                                                                                                                                          |
| SETTLE_PRICE

          | double

         | Settlement price

                                                                                                                                                                                                                       |
### ABAXX - MKT

Market phase / instrument status information

### ABAXX - MKT Table Schema

| Field

                 | Data Type

      | Description

                                                                                                                                                                                                                            |
| --------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MKT_PHASE

             | string[20]

     | Indicates the instrument’s current market phase, as specified by the trading venue

                                                                                                                                                     |
| OMDSEQ

                | uint

           | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

 |
| OMD_STATUS

            | string[1]

      | Indicates an instrument’s current trading status. Values are normalized across all DBs.

                                                                                                                                                |
| TRADING_DATE

          | string[8]

      | Identifies the current business date (YYYYMMDD). May be different to the calendar date, e.g. for T+1 trading sessions.

                                                                                                                 |
### ABAXX - QTE

Best bid / offer quotes

### ABAXX - QTE Table Schema

| Field

                 | Data Type

      | Description

                                                                                                                                                                                                                            |
| --------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_PRICE

             | double

         | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                       |
| ASK_SIZE

              | int

            | Best ask size

                                                                                                                                                                                                                          |
| BID_PRICE

             | double

         | Best bid price. A null value is used if the bid side is empty, or if the best bid is set by unpriced orders (e.g. market orders)

                                                                                                       |
| BID_SIZE

              | int

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
### ABAXX - STAT

Static data, e.g. ISIN, description, security type

### ABAXX - STAT Table Schema

| Field

                 | Data Type

      | Description

                                                                                                                                                                                                                            |
| --------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CONTRACT_SIZE

         | double

         | Indicates a derivative’s underlying quantity

                                                                                                                                                                                           |
| CURRENCY

              | string[3]

      | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                        |
| DELIVERY_END_DATE

     | string[8]

      | Date when a derivative’s delivery period ends (YYYYMMDD)

                                                                                                                                                                               |
| DELIVERY_START_DATE

   | string[8]

      | Date when a derivative’s delivery period begins (YYYYMMDD)

                                                                                                                                                                             |
| EXCH_SEC_TYPE

         | string[20]

     | Instrument type as specified by the exchange

                                                                                                                                                                                           |
| EXCH_SYMBOL

           | string[32]

     | Ticker symbol specified by the exchange

                                                                                                                                                                                                |
| EXPIRATION_DATE

       | string[8]

      | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                              |
| LAST_TRADING_TIME

     | nsectime

       | Time when the instrument finishes trading on the final trading day

                                                                                                                                                                     |
| MAX_TRADE_SIZE

        | int

            | Maximum tradable size

                                                                                                                                                                                                                  |
| MIC

                   | string[4]

      | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

                                                                                                                                       |
| MIN_TRADE_SIZE

        | int

            | Minimum tradable size

                                                                                                                                                                                                                  |
| NAME

                  | string[200]

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

          | string[12]

     | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.

 |
| SEC_TYPE

              | string[20]

     | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                    |
| SETTLEMENT_TYPE

       | string[1]

      | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)

                                                                                                                                         |
| STRATEGY_LEGS

         | string[200]

    | Comma-separated list of symbols for the legs of a futures / options spread

                                                                                                                                                                 |
| STRATEGY_LEG_COUNT

    | int

            | Number of legs in a strategy (spread)

                                                                                                                                                                                                      |
| TICK_SIZE

             | double

         | Tick size / minimum price increment. All order prices must be a multiple of the tick size.

                                                                                                                                                 |
| TRADING_CODE

          | string[20]

     | ID used to identify the instrument in the trading system

                                                                                                                                                                                   |
| UNDERLYING_SEC_TYPE

   | string[20]

     | Underlying asset class

                                                                                                                                                                                                                     |
### ABAXX - TRD

Trades

### ABAXX - TRD Table Schema

| Field

                 | Data Type

      | Description

                                                                                                                                                                                                                                |
| --------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| AGGRESSOR_SIDE

        | string[1]

      | Indicates whether a trade resulted from an incoming buy or sell order.

                                                                                                                                                                     |
| BOOK_TYPE

             | string[1]

      | Type of order book or trading mechanism through which a trade was executed.

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

                  | int

            | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                           |
| TRADE_TYPE

            | string[4]

      | Type of trade

