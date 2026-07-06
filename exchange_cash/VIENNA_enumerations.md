# Vienna Stock Exchange Enumerations

The Vienna Stock Exchange is the only stock exchange in Austria trading Austrian equities and bonds.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


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

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                                 | Lit order book

                                                                                                                             |
| 1

                                 | Off-book

                                                                                                                                   |
| 2

                                 | Dark book

                                                                                                                                  |
| Q

                                 | Quote-driven trading

                                                                                                                       |
| ‘””’

                              | Not applicable

                                                                                                                             |
# MKT_PHASE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 1

                                 | Closed

                                                                                                                                     |
| 1001

                              | Opening auction

                                                                                                                            |
| 1002

                              | Intraday auction

                                                                                                                           |
| 1003

                              | Closing auction

                                                                                                                            |
| 1006

                              | Volatility auction

                                                                                                                         |
| 1007

                              | Extended volatility auction

                                                                                                                |
| 1008

                              | Opening auction call

                                                                                                                       |
| 1009

                              | Opening auction pre-orderbook balancing

                                                                                                    |
| 1010

                              | Opening auction orderbook balancing

                                                                                                        |
| 1011

                              | Intraday auction call

                                                                                                                      |
| 1012

                              | Intraday auction pre-orderbook balancing

                                                                                                   |
| 1013

                              | Intraday auction orderbook balancing

                                                                                                       |
| 1014

                              | Closing auction call

                                                                                                                       |
| 1015

                              | Closing auction pre-orderbook balancing

                                                                                                    |
| 1016

                              | Closing auction orderbook balancing

                                                                                                        |
| 1017

                              | Initial state prior to first trading day

                                                                                                   |
| 1018

                              | Final state after last trading day

                                                                                                         |
| 1019

                              | Continuous auction pre-call

                                                                                                                |
| 1020

                              | Continuous auction call

                                                                                                                    |
| 1021

                              | Pre-trade mass

                                                                                                                             |
| 1022

                              | Trade mass

                                                                                                                                 |
| 1027

                              | Halted

                                                                                                                                     |
| 1028

                              | Post-trading

                                                                                                                               |
| 1029

                              | Potential volatility interruption

                                                                                                          |
| 1030

                              | Volatility auction uncrossing

                                                                                                              |
| 1031

                              | Market order interruption

                                                                                                                  |
| 1032

                              | Potential market order interruption

                                                                                                        |
| 1033

                              | Trading at close

                                                                                                                           |
| 2

                                 | Pre-trading

                                                                                                                                |
| 32

                                | Start of day

                                                                                                                               |
| 6

                                 | Continuous trading

                                                                                                                         |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a cross trade

                                                                                                                          |
| X

                                 | Agency cross trade

                                                                                                                         |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 1

                                 | Central Limit Order Book

                                                                                                                   |
| 2

                                 | Quote-Driven Market

                                                                                                                        |
| 3

                                 | Dark Book

                                                                                                                                  |
| 4

                                 | Off Book

                                                                                                                                   |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| 4

                                 | Pre-trade transparency waiver for illiquid instrument on an SI

                                                                             |
| 5

                                 | Pre-trade transparency waiver for trade larger than Standard Market Size on an SI

                                                          |
| 6

                                 | Pre-trade transparency waivers for trade larger than Standard Market Size on an SI and illiquid instrument on an SI

                        |
| N

                                 | Negotiated trade

                                                                                                                           |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| D

                                 | Dark trade

                                                                                                                                 |
| Y

                                 | Exchange for physical

                                                                                                                      |
| Z

                                 | Package trade

                                                                                                                              |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 2

                                 | Continuous trading

                                                                                                                         |
| 3

                                 | At Market Close trading

                                                                                                                    |
| 5

                                 | Trade reporting (on-exchange)

                                                                                                              |
| I

                                 | Intraday auction

                                                                                                                           |
| K

                                 | Closing auction

                                                                                                                            |
| O

                                 | Opening auction

                                                                                                                            |
| U

                                 | Unscheduled auction

                                                                                                                        |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Other auction [e.g. after-hours odd lot auction]

                                                                                           |
| C

                                 | Closing auction

                                                                                                                            |
| I

                                 | Intraday auction

                                                                                                                           |
| O

                                 | Opening auction

                                                                                                                            |
| T

                                 | Trading at closing price

                                                                                                                   |
| U

                                 | Unscheduled auction

                                                                                                                        |
| -

                                 | Regular trading

                                                                                                                            |
| ‘””’

                              | Not applicable

                                                                                                                             |
# TRADE_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| a

                                 | Continuous trading

                                                                                                                         |
| b

                                 | Opening auction

                                                                                                                            |
| c

                                 | Intraday auction

                                                                                                                           |
| d

                                 | Closing auction

                                                                                                                            |
| f

                                 | Volatility auction

                                                                                                                         |
| g

                                 | Trade at close

                                                                                                                             |
| h

                                 | Price without turnover [valuation trade]

                                                                                                   |
| i

                                 | Negotiated trade

                                                                                                                           |
| M

                                 | Midpoint trade

                                                                                                                             |
| p

                                 | OTC trade

                                                                                                                                  |
| q

                                 | Negotiated OTC trade

                                                                                                                       |
| v

                                 | Continuous auction

                                                                                                                         |
| w

                                 | Reference price

