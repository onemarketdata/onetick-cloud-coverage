# Aquis Europe Enumerations

Aquis Europe is the European segment of the Aquis pan-European cash equities trading books, covering securities across 13 European markets outside the UK.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* TRADING_STATUS - Indicates whether the instrument is subject to a halt or suspension


* UPDATE_TYPE - Type of update

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                        | Undefined (e.g. auction trades, off-book trades)

                                                                    |
| B

                           | Buy

                                                                                                                 |
| S

                           | Sell

                                                                                                                |
# BOOK_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Lit order book

                                                                                                      |
| 1

                           | Off-book

                                                                                                            |
| 2

                           | Dark book

                                                                                                           |
| 6

                           | Auction book

                                                                                                        |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Closed

                                                                                                              |
| 1

                           | Open

                                                                                                                |
| 2

                           | Market at Close call phase

                                                                                          |
| 6

                           | Market at Close uncrossing

                                                                                          |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not an algorithmic trade

                                                                                            |
| H

                           | Algorithmic trade

                                                                                                   |
# MMT_BENCHMARK_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not a benchmark trade

                                                                                               |
| B

                           | Benchmark trade

                                                                                                     |
| S

                           | Reference price trade

                                                                                               |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not a cross trade

                                                                                                   |
| X

                           | Agency cross trade

                                                                                                  |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | No deferral / unspecified

                                                                                           |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| E

                           | Ex-/cum-dividend

                                                                                                    |
# MMT_DUP_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Unique trade report

                                                                                                 |
| 1

                           | Duplicative trade reported to more than one APA

                                                                     |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Central Limit Order Book

                                                                                            |
| 4

                           | Off Book

                                                                                                            |
| 5

                           | Periodic Auction

                                                                                                    |
# MMT_MOD_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | New trade

                                                                                                           |
| A

                           | Amended trade

                                                                                                       |
| C

                           | Trade cancellation

                                                                                                  |
# MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| 1

                           | Negotiated trade in liquid instruments

                                                                              |
| 2

                           | Negotiated trade in illiquid instruments

                                                                            |
| 3

                           | Negotiated trade subject to conditions other than the market price

                                                  |
| N

                           | Negotiated trade

                                                                                                    |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| M

                           | Off-book manual

                                                                                                     |
| Q

                           | Off-book automated

                                                                                                  |
# MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| J

                           | Trade not contributing to the price discovery process

                                                               |
| N

                           | Price not available but pending

                                                                                     |
| P

                           | Plain vanilla (price-forming) trade

                                                                                 |
| T

                           | Non-price forming (technical) trade

                                                                                 |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Immediate publication

                                                                                               |
| 1

                           | Delayed publication / late reported

                                                                                 |
| 2

                           | Deferred publication (Large in Scale)

                                                                               |
| 3

                           | Deferred publication (illiquid instrument)

                                                                          |
| 4

                           | Deferred publication (size specific to instrument)

                                                                  |
| 5

                           | Deferred publication (illiquid instrument and size specific to instrument)

                                          |
| 6

                           | Deferred publication (illiquid instrument and Large in Scale)

                                                       |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                      |
| D

                           | Dark trade [hidden order execution]

                                                                                 |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 2

                           | Continuous trading

                                                                                                  |
| 5

                           | Trade reporting (on-exchange)

                                                                                       |
| 6

                           | Trade reporting (off-exchange)

                                                                                      |
| K

                           | Closing auction

                                                                                                     |
| U

                           | Unscheduled auction

                                                                                                 |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| C

                           | Closing Auction

                                                                                                     |
| U

                           | Unscheduled Auction

                                                                                                 |
| p

                           | Auction initiated by market participant

                                                                             |
| -

                           | Regular trading

                                                                                                     |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Lit order execution

                                                                                                 |
| 2

                           | Hidden order execution

                                                                                              |
| 3

                           | Market at Close trade

                                                                                               |
| 4

                           | Large in Scale (LIS) Cross trade

                                                                                    |
| 5

                           | Benchmark Cross trade

                                                                                               |
| 6

                           | Auction on Demand trade

                                                                                             |
# TRADING_STATUS - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Active

                                                                                                              |
| 2

                           | Halted

                                                                                                              |
| 3

                           | Suspended

                                                                                                           |
# UPDATE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| A

                           | Add

                                                                                                                 |
| D

                           | Delete

                                                                                                              |
| F

                           | Fill

                                                                                                                |
| M

                           | Modify

                                                                                                              |
| P

                           | Partial Fill

