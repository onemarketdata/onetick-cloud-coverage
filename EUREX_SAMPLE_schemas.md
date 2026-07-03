# Eurex Sample Schemas

A subset of symbols from Eurex covering Futures for products FDAX (DAX), FESX (Euro Stoxx 50 Index), FTUK (FTSE 100 Index).   Between January 2,2024 and March 31, 2024

## EUREX_SAMPLE

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* IND - Indicative pricing, e.g. indicative auction prices and imbalance


* MKT - Market phase / instrument status information


* QTE - Best bid / offer quotes


* SEC_GROUP -  Group Reference


* STAT - Static data, e.g. ISIN, description, security type


* TRD - Trades

### EUREX_SAMPLE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### EUREX_SAMPLE - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| OPEN_INT_DATE

               | string[8]

                                                                                                                         | Trading date to which the open interest relates (YYYYMMDD)

                                                                                                                                                                                        |
| SETTLE_DATE

                 | string[8]

                                                                                                                         | Trading date to which the settlement price relates (YYYYMMDD)

                                                                                                                                                                                     |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                  |
| UPDATE_TYPE

                 | string[16]

                                                                                                                        | Type of update

                                                                                                                                                                                                                                    |
| VOLUME

                      | double

                                                                                                                            | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### EUREX_SAMPLE - IND

Indicative pricing, e.g. indicative auction prices and imbalance

### EUREX_SAMPLE - IND Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AUCTION_TYPE

                | string[1]

                                                                                                                         | Type of auction from which an indicative auction price / auction imbalance originates.

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
### EUREX_SAMPLE - MKT

Market phase / instrument status information

### EUREX_SAMPLE - MKT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXCH_TIME

                   | nsectime

                                                                                                                          | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| MKT_COND

                    | string[4]

                                                                                                                         | Indicates any unusual market conditions

                                                                                                                                                                                                           |
| MKT_PHASE

                   | string[12]

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
### EUREX_SAMPLE - QTE

Best bid / offer quotes

### EUREX_SAMPLE - QTE Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASK_COND

                    | string[1]

                                                                                                                         | Quote condition applicable to the best ask

                                                                                                                                                                                                        |
| ASK_PRICE

                   | double

                                                                                                                            | Best ask price. A null value is used if the ask side is empty, or if the best ask is set by unpriced orders (e.g. market orders)

                                                                                                                  |
| ASK_SIZE

                    | int

                                                                                                                               | Best ask size

                                                                                                                                                                                                                                     |
| BID_COND

                    | string[1]

                                                                                                                         | Quote condition applicable to the best bid

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
### EUREX_SAMPLE - SEC_GROUP

> Group Reference

### EUREX_SAMPLE - SEC_GROUP Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GROUP_SYMBOL

                | string[32]

                                                                                                                        | Security Group for Options Contract

                                                                                                                                                                                                               |
| OMDSEQ

                      | uint

                                                                                                                              | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
### EUREX_SAMPLE - STAT

Static data, e.g. ISIN, description, security type

### EUREX_SAMPLE - STAT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CALL_PUT_IND

                | string[1]

                                                                                                                         | C - Call option, P - Put option

                                                                                                                                                                                                                   |
| CFI_CODE

                    | string[6]

                                                                                                                         | Classification of Financial Instruments code (ISO 10962), indicating the type of security

                                                                                                                                                         |
| CONTRACT_SIZE

               | double

                                                                                                                            | Indicates a derivative’s underlying quantity

                                                                                                                                                                                                      |
| CURRENCY

                    | string[3]

                                                                                                                         | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_STRATEGY_TYPE

          | string[12]

                                                                                                                        | Type of strategy / spread, as specified by the exchange

                                                                                                                                                                                           |
| EXCH_SYMBOL

                 | string[48]

                                                                                                                        | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| EXERCISE_TYPE

               | string[1]

                                                                                                                         | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)

                                                                                                                                                                        |
| EXPIRATION_DATE

             | string[8]

                                                                                                                         | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                                         |
| ISIN

                        | string[12]

                                                                                                                        | ISIN code

                                                                                                                                                                                                                                         |
| MIC

                         | string[4]

                                                                                                                         | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

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

                | string[20]

                                                                                                                        | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.

        |
| PRODUCT_ISIN

                | string[12]

                                                                                                                        | Pseudo-ISIN assigned to a futures / options product

                                                                                                                                                                                               |
| SEC_TYPE

                    | string[32]

                                                                                                                        | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
| SETTLEMENT_TYPE

             | string[1]

                                                                                                                         | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)

                                                                                                                                                |
| STRATEGY_TYPE

               | string[48]

                                                                                                                        | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly

                                                                                                                                                                                |
| STRIKE_PRICE

                | double

                                                                                                                            | Exercise price for options / warrants

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
| TRADING_CODE

                | string[20]

                                                                                                                        | ID used to identify the instrument in the trading system

                                                                                                                                                                                          |
| UNDERLYING_ISIN

             | string[12]

                                                                                                                        | ISIN of the underlying instrument

                                                                                                                                                                                                                 |
| UNDERLYING_SEC_TYPE

         | string[20]

                                                                                                                        | Underlying asset class

                                                                                                                                                                                                                            |
| UNDERLYING_SYMBOL

           | string[32]

                                                                                                                        | Symbol of the underlying instrument

                                                                                                                                                                                                               |
### EUREX_SAMPLE - TRD

Trades

### EUREX_SAMPLE - TRD Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AGGRESSOR_SIDE

              | string[1]

                                                                                                                         | Indicates whether a trade resulted from an incoming buy or sell order.

                                                                                                                                                                            |
| DELETED_TIME

                | nsectime

                                                                                                                          | Internal OneTick field. Usually null unless hidden ticks are requested (e.g. SHOW_HIDDEN_TICKS).

                                                                                                                                                  |
| EXCH_TIME

                   | nsectime

                                                                                                                          | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| MMT_ALGO_IND

                | string[1]

                                                                                                                         | Identifies whether a trade involved an algorithmic order.

                                                                                                                                                                                         |
| MMT_BENCHMARK_IND

           | string[1]

                                                                                                                         | Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).

 |
| MMT_CROSS_IND

               | string[1]

                                                                                                                         | Identifies agency cross trades, where a broker crossed two client orders outside the order book.

                                                                                                                                                  |
| MMT_DEFERRAL_TYPE

           | string[1]

                                                                                                                         | Type of publication deferral or subsequent enrichment applied to a trade report.

                                                                                                                                                                  |
| MMT_DIVIDEND_IND

            | string[1]

                                                                                                                         | Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.

                                                                                                                   |
| MMT_DUP_IND

                 | string[1]

                                                                                                                         | Identifies trades reported to more than one Approved Publication Arrangement.

                                                                                                                                                                     |
| MMT_MKT_MECH

                | string[1]

                                                                                                                         | Market mechanism through which a trade was executed.

                                                                                                                                                                                              |
| MMT_MOD_IND

                 | string[1]

                                                                                                                         | Identifies trade cancellations, or amendments of a previous trade.

                                                                                                                                                                                |
| MMT_NEGOTIATED_IND

          | string[1]

                                                                                                                         | Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.

                                                                                                                                      |
| MMT_OFF_BOOK_AUTO_IND

       | string[1]

                                                                                                                         | Identifies whether an off-book trade report was executed via a manual or automated process.

                                                                                                                                                       |
| MMT_PRICE_FORMING_IND

       | string[1]

                                                                                                                         | Identifies whether a trade is price-forming, or contributes to the price discovery process.

                                                                                                                                                       |
| MMT_PUB_MODE

                | string[1]

                                                                                                                         | Identifies whether a trade was subject to delayed publication, and the reason for the deferral.

                                                                                                                                                   |
| MMT_TRANS_CAT

               | string[1]

                                                                                                                         | Identifies various special categories of trade.

                                                                                                                                                                                                   |
| MMT_TRD_MODE

                | string[1]

                                                                                                                         | Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).

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
| TRADE_ID

                    | string[16]

                                                                                                                        | Trade identifier, generally the ID assigned by the matching engine

                                                                                                                                                                                |
| TRADE_TYPE

                  | string[4]

                                                                                                                         | Type of trade

                                                                                                                                                                                                                                     |
| TRADE_VENUE

                 | string[4]

                                                                                                                         | Identifies the venue where a trade was executed.   Typically a MIC, with the special values XOFF for off-exchange and SINT for Systematic Internaliser trades.

                                                                                    |
## EUREX_SAMPLE_BARS

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* MKT - Market phase / instrument status information


* QTE_1M - 1-minute quote bars


* TRD_1D - Daily trade bars


* TRD_1M - 1-minute trade bars


* VWAP_1H - 1-hour VWAP bars

### EUREX_SAMPLE_BARS - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### EUREX_SAMPLE_BARS - DAY Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OPEN_INT_DATE

               | string[8]

                                                                                                                         | Trading date to which the open interest relates (YYYYMMDD)

                                                                                                                                                                                        |
| SETTLE_DATE

                 | string[8]

                                                                                                                         | Trading date to which the settlement price relates (YYYYMMDD)

                                                                                                                                                                                     |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                  |
| UPDATE_TYPE

                 | string[16]

                                                                                                                        | Type of update

                                                                                                                                                                                                                                    |
| VOLUME

                      | double

                                                                                                                            | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### EUREX_SAMPLE_BARS - MKT

Market phase / instrument status information

### EUREX_SAMPLE_BARS - MKT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EXCH_TIME

                   | nsectime

                                                                                                                          | Event timestamp, as provided by the exchange. For electronic trading this refers to the matching engine timestamp

                                                                                                                                 |
| MKT_COND

                    | string[4]

                                                                                                                         | Indicates any unusual market conditions

                                                                                                                                                                                                           |
| MKT_PHASE

                   | string[12]

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
### EUREX_SAMPLE_BARS - QTE_1M

1-minute quote bars

### EUREX_SAMPLE_BARS - QTE_1M Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### EUREX_SAMPLE_BARS - TRD_1D

Daily trade bars

### EUREX_SAMPLE_BARS - TRD_1D Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### EUREX_SAMPLE_BARS - TRD_1M

1-minute trade bars

### EUREX_SAMPLE_BARS - TRD_1M Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
### EUREX_SAMPLE_BARS - VWAP_1H

1-hour VWAP bars

### EUREX_SAMPLE_BARS - VWAP_1H Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
## EUREX_SAMPLE_DAILY

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* STAT - Static data, e.g. ISIN, description, security type

### EUREX_SAMPLE_DAILY - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### EUREX_SAMPLE_DAILY - DAY Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
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
| OPEN_INT_DATE

               | string[8]

                                                                                                                         | Trading date to which the open interest relates (YYYYMMDD)

                                                                                                                                                                                        |
| SETTLE_DATE

                 | string[8]

                                                                                                                         | Trading date to which the settlement price relates (YYYYMMDD)

                                                                                                                                                                                     |
| SETTLE_PRICE

                | double

                                                                                                                            | Settlement price

                                                                                                                                                                                                                                  |
| UPDATE_TYPE

                 | string[16]

                                                                                                                        | Type of update

                                                                                                                                                                                                                                    |
| VOLUME

                      | double

                                                                                                                            | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### EUREX_SAMPLE_DAILY - STAT

Static data, e.g. ISIN, description, security type

### EUREX_SAMPLE_DAILY - STAT Table Schema

| Field

                       | Data Type

                                                                                                                         | Description

                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CALL_PUT_IND

                | string[1]

                                                                                                                         | C - Call option, P - Put option

                                                                                                                                                                                                                   |
| CFI_CODE

                    | string[6]

                                                                                                                         | Classification of Financial Instruments code (ISO 10962), indicating the type of security

                                                                                                                                                         |
| CONTRACT_SIZE

               | double

                                                                                                                            | Indicates a derivative’s underlying quantity

                                                                                                                                                                                                      |
| CURRENCY

                    | string[3]

                                                                                                                         | Currency in which the instrument’s price is expressed (or nominal currency for bonds traded as a % of nominal).

                                                                                                                                   |
| EXCH_STRATEGY_TYPE

          | string[12]

                                                                                                                        | Type of strategy / spread, as specified by the exchange

                                                                                                                                                                                           |
| EXCH_SYMBOL

                 | string[48]

                                                                                                                        | Ticker symbol specified by the exchange

                                                                                                                                                                                                           |
| EXERCISE_TYPE

               | string[1]

                                                                                                                         | Option exercise type (A - American, E - European, B - Bermudan, S - Asian)

                                                                                                                                                                        |
| EXPIRATION_DATE

             | string[8]

                                                                                                                         | Date when a derivative expires (YYYYMMDD)

                                                                                                                                                                                                         |
| ISIN

                        | string[12]

                                                                                                                        | ISIN code

                                                                                                                                                                                                                                         |
| MIC

                         | string[4]

                                                                                                                         | Market Identifier Code (MIC, ISO 10383) identifying the market on which the instrument is traded

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

                | string[20]

                                                                                                                        | Root code of a futures / options product, as specified by the exchange (e.g. CL for Crude Oil futures on NYMEX).   For inter-product spreads, PRODUCT_CODE will include both products, e.g. AB-CD for a spread between products AB and CD.

        |
| PRODUCT_ISIN

                | string[12]

                                                                                                                        | Pseudo-ISIN assigned to a futures / options product

                                                                                                                                                                                               |
| SEC_TYPE

                    | string[32]

                                                                                                                        | Security type, e.g. Equity, ETF, Future

                                                                                                                                                                                                           |
| SETTLEMENT_TYPE

             | string[1]

                                                                                                                         | Settlement method for a derivatives contract (C - Cash, P - Physical, E - Either cash or physical)

                                                                                                                                                |
| STRATEGY_TYPE

               | string[48]

                                                                                                                        | Type of strategy / spread, e.g. Calendar Spread, Futures Butterfly

                                                                                                                                                                                |
| STRIKE_PRICE

                | double

                                                                                                                            | Exercise price for options / warrants

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
| TRADING_CODE

                | string[20]

                                                                                                                        | ID used to identify the instrument in the trading system

                                                                                                                                                                                          |
| UNDERLYING_ISIN

             | string[12]

                                                                                                                        | ISIN of the underlying instrument

                                                                                                                                                                                                                 |
| UNDERLYING_SEC_TYPE

         | string[20]

                                                                                                                        | Underlying asset class

                                                                                                                                                                                                                            |
| UNDERLYING_SYMBOL

           | string[32]

                                                                                                                        | Symbol of the underlying instrument

