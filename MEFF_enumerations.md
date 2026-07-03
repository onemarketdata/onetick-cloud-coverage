# MEFF Exchange Enumerations

MEFF is the Spanish derivatives exchange, offering trading in futures and options on Spanish equities, indices, and interest rates.

The following fields have Enumerations:


* CALL_PUT_IND - “C” - Call option, “P” - Put option


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* TRADE_TYPE - Type of trade

# CALL_PUT_IND - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| C

                           | Call option

                                                                                                                       |
| P

                           | Put option

                                                                                                                        |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Pre-trading

                                                                                                                       |
| 100

                         | Trading at closing price

                                                                                                          |
| 101

                         | End of closing auction

                                                                                                            |
| 102

                         | Closing price calculation

                                                                                                         |
| 2

                           | Opening auction

                                                                                                                   |
| 202

                         | Not started

                                                                                                                       |
| 203

                         | Open

                                                                                                                              |
| 204

                         | Closed

                                                                                                                            |
| 3

                           | Continuous trading

                                                                                                                |
| 4

                           | Closing auction

                                                                                                                   |
| 5

                           | Post-trading

                                                                                                                      |
| 6

                           | Intraday auction

                                                                                                                  |
| 9

                           | Unscheduled auction

                                                                                                               |
| A

                           | Accepting orders

                                                                                                                  |
| a

                           | Auction

                                                                                                                           |
| B

                           | Break

                                                                                                                             |
| C

                           | Closed

                                                                                                                            |
| c

                           | Extended closing auction

                                                                                                          |
| E

                           | Post-trading

                                                                                                                      |
| H

                           | Halted

                                                                                                                            |
| I

                           | Intraday auction

                                                                                                                  |
| L

                           | Closing auction

                                                                                                                   |
| m

                           | Manual auction

                                                                                                                    |
| M

                           | Pre-trading

                                                                                                                       |
| n

                           | Not tradable

                                                                                                                      |
| o

                           | Extended opening auction

                                                                                                          |
| r

                           | Halted by Regulator

                                                                                                               |
| s

                           | Halted by Market Surveillance

                                                                                                     |
| T

                           | Continuous trading

                                                                                                                |
| U

                           | Underlying halted

                                                                                                                 |
| V

                           | Suspended

                                                                                                                         |
| v

                           | Volatility auction

                                                                                                                |
| Z

                           | Trading at last price

                                                                                                             |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | No deferral / unspecified

                                                                                                         |
| 1

                           | Limited details

                                                                                                                   |
| 2

                           | Daily aggregated trade

                                                                                                            |
| 3

                           | Volume omission trade

                                                                                                             |
| 4

                           | 4 weeks aggregated trade

                                                                                                          |
| 5

                           | Indefinite aggregated trade

                                                                                                       |
| 6

                           | Volume omission trade eligible for enrichment in aggregated form

                                                                  |
| 7

                           | Full details of earlier Limited Details trade

                                                                                     |
| 8

                           | Full details of earlier Daily Aggregated trade

                                                                                    |
| 9

                           | Full details of earlier Volume Omission trade

                                                                                     |
| V

                           | Full details of 4 Weeks Aggregated trade

                                                                                          |
| W

                           | Full details of Volume Omission trade eligible for enrichment in aggregated form

                                                  |
# MMT_DUP_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Unique trade report

                                                                                                               |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Central Limit Order Book

                                                                                                          |
| 4

                           | Off Book

                                                                                                                          |
| 6

                           | Request for Quote

                                                                                                                 |
# MMT_MOD_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not a negotiated trade

                                                                                                            |
| 1

                           | Negotiated trade in liquid instruments

                                                                                            |
| 2

                           | Negotiated trade in illiquid instruments

                                                                                          |
| 3

                           | Negotiated trade subject to conditions other than the current market price

                                                        |
| N

                           | Negotiated trade

                                                                                                                  |
# MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Immediate publication

                                                                                                             |
| 1

                           | Delayed publication (including late reported)

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
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| -

                           | Not applicable

                                                                                                                    |
| Z

                           | Package trade

                                                                                                                     |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1

                           | Auction

                                                                                                                           |
| 2

                           | Continuous trading

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
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Regular trade

                                                                                                                     |
| 1

                           | Cross trade (outside hours) [until 20221117]

                                                                                      |
| 2

                           | Cross trade

                                                                                                                       |
| 3

                           | Delta trade

                                                                                                                       |
| 4

                           | Spread trade [until 20241231]

                                                                                                     |
| 5

                           | Strategy leg trade

                                                                                                                |
| RFQ

                         | RFQ trade

