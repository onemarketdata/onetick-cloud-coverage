# Stuttgart Stock Exchange Enumerations

Börse Stuttgart is the leading stock exchange for structured securities and corporate bond trading in Germany

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* CLEARED - Cleared


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                              | Not applicable

                                                                                                                             |
| 1

                                 | Off-book

                                                                                                                                   |
| 9

                                 | Off-exchange

                                                                                                                               |
| Q

                                 | Quote-driven trading

                                                                                                                       |
| R

                                 | Request for Quote

                                                                                                                          |
# CLEARED - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Y

                                 | To be cleared

                                                                                                                              |
| N

                                 | Not to be cleared

                                                                                                                          |
| ‘””’

                              | Not specified

                                                                                                                              |
# MKT_PHASE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Quoting suspended due to auction

                                                                                                           |
| E

                                 | Quoting during pre-trade phase but no trading

                                                                                              |
| I

                                 | Volatility halt

                                                                                                                            |
| M

                                 | Market segment suspended

                                                                                                                   |
| N

                                 | Not trading due to no quotes from designated market maker

                                                                                  |
| P

                                 | Quoting during post-trade phase but no trading

                                                                                             |
| Q

                                 | Active and quoted data is in response to an RFQ

                                                                                            |
| S

                                 | Suspended by trading system

                                                                                                                |
| T

                                 | Active and trading

                                                                                                                         |
| X

                                 | Quoting suspended due to system shutdown

                                                                                                   |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 2

                                 | Quote Driven Market

                                                                                                                        |
| 4

                                 | Off Book

                                                                                                                                   |
| 6

                                 | Request for Quote

                                                                                                                          |
| 7

                                 | Other / Hybrid

                                                                                                                             |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 2

                                 | Continuous trading

                                                                                                                         |
| 5

                                 | Trade reporting (on-exchange)

                                                                                                              |
| 6

                                 | Trade reporting (off-exchange)

                                                                                                             |
| U

                                 | Unscheduled auction

                                                                                                                        |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
# MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| N

                                 | Negotiated trade

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
| -

                                 | Not applicable

                                                                                                                             |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a cross trade

                                                                                                                          |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Amended trade

                                                                                                                              |
| C

                                 | Trade cancellation

                                                                                                                         |
| -

                                 | New trade

                                                                                                                                  |
# MMT_BENCHMARK_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

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
| Z

                                 | Price not applicable

                                                                                                                       |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| H

                                 | Algorithmic trade

                                                                                                                          |
| -

                                 | Not an algorithmic trade

                                                                                                                   |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Immediate publication

                                                                                                                      |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | No deferral / unspecified

                                                                                                                  |
# MMT_DUP_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Unique trade report

                                                                                                                        |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | Not applicable

                                                                                                                             |
| A

                                 | Auction

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
| U

                                 | Unscheduled auction

                                                                                                                        |
| -

                                 | Regular trading

                                                                                                                            |
# TRADE_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | No condition

                                                                                                                               |
| B

                                 | Ask

                                                                                                                                        |
| BB

                                | Paid, unexecuted sell orders

                                                                                                               |
| BF

                                | Ask, Bundesbank fixing

                                                                                                                     |
| BG

                                | Paid, unexecuted buy orders

                                                                                                                |
| BP

                                | Ask, primary market price

                                                                                                                  |
| BZ

                                | Paid, all orders executed

                                                                                                                  |
| BZF

                               | Paid, Bundesbank fixing

                                                                                                                    |
| BZP

                               | Paid, primary market transaction

                                                                                                           |
| C

                                 | Cross trade

                                                                                                                                |
| EB

                                | Partially paid, only a small portion of sell orders were executed

                                                                          |
| EG

                                | Partially paid, only a small portion of buy orders were executed

                                                                           |
| F

                                 | Bundesbank fixing

                                                                                                                          |
| G

                                 | Bid

                                                                                                                                        |
| GF

                                | Bid, Bundesbank fixing

                                                                                                                     |
| GP

                                | Bid, primary market price

                                                                                                                  |
| OTC

                               | OTC trade

                                                                                                                                  |
| RB

                                | Partial execution on buy side

                                                                                                              |
| RB\*

                               | Partial execution on buy side, orders allocated based on time of entry

                                                                     |
| RG

                                | Partial execution on sell side

                                                                                                             |
| RG\*

                               | Partial execution on sell side, orders allocated based on time of entry

                                                                    |
| 
*                                   | Small amounts could not be traded

                                                                                                          |
| _BT

                               | Estimated price, excess orders on ask side

                                                                                                 |
| _GT

                               | Estimated price, excess orders on bid side

                                                                                                 |
| _T

                                | Estimated price

