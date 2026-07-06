# Equiduct Exchange Enumerations

Equiduct is a pan-European regulated market and MTF owned by Boerse Berlin, providing trading in over 6,000 equities and ETFs across 12 European markets.

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


* ORDER_TYPE - Type of order.


* REASON_CODE - Reason for an instrument status update


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* UPDATE_TYPE - Type of update

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                             | Lit order book

                                                                                                         |
| 1

                             | Off-book

                                                                                                               |
# MKT_PHASE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| A

                             | Auction

                                                                                                                |
| H

                             | Halted

                                                                                                                 |
| T

                             | Trading

                                                                                                                |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Not applicable

                                                                                                         |
| 1

                             | Benchmark trade executed at the closing price

                                                                          |
| 2

                             | Portfolio trade + benchmark trade executed at the closing price

                                                        |
| 3

                             | Contingent trade + benchmark trade executed at the closing price

                                                       |
| 4

                             | Contingent trade + portfolio trade + benchmark trade executed at the closing price

                                     |
| B

                             | Benchmark trade

                                                                                                        |
| C

                             | Contingent trade

                                                                                                       |
| M

                             | Benchmark trade + contingent trade

                                                                                     |
| N

                             | Contingent trade + portfolio trade

                                                                                     |
| O

                             | Benchmark trade + contingent trade + portfolio trade

                                                                   |
| P

                             | Portfolio trade

                                                                                                        |
| S

                             | Reference price trade

                                                                                                  |
| Y

                             | Benchmark trade + portfolio trade

                                                                                      |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Not a cross trade

                                                                                                      |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | No deferral / unspecified

                                                                                              |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Not applicable

                                                                                                         |
# MMT_DUP_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | Unique trade report

                                                                                                    |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1

                             | Central Limit Order Book

                                                                                               |
| 4

                             | Off Book

                                                                                                               |
| 8

                             | Hybrid

                                                                                                                 |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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

                             | Negotiated trade subject to conditions other than the current market price

                                             |
| N

                             | Negotiated trade

                                                                                                       |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| P

                             | Plain vanilla (price-forming) trade

                                                                                    |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                             | No condition

                                                                                                           |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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
# ORDER_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| L

                             | Limit order

                                                                                                            |
# REASON_CODE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | Unspecified

                                                                                                            |
| AC

                            | Closing procedure

                                                                                                      |
| ACF

                           | Closing freeze (prior to uncrossing)

                                                                                   |
| AE

                            | Auction due to external market status

                                                                                  |
| AO

                            | Opening procedure

                                                                                                      |
| AOF

                           | Opening freeze

                                                                                                         |
| AU

                            | Unscheduled auction

                                                                                                    |
| AUM

                           | Market order extension

                                                                                                 |
| AUV

                           | Volatliity extension

                                                                                                   |
| AV

                            | Volatility auction

                                                                                                     |
| C

                             | Closed

                                                                                                                 |
| CC

                            | Post-close

                                                                                                             |
| CO

                            | Pre-trading

                                                                                                            |
| H

                             | Halted

                                                                                                                 |
| HE

                            | Halted due to external market status

                                                                                   |
| S

                             | Suspended

                                                                                                              |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| A

                             | Auction

                                                                                                                |
| C

                             | Closing Auction

                                                                                                        |
| I

                             | Intraday Auction

                                                                                                       |
| O

                             | Opening Auction

                                                                                                        |
| U

                             | Unscheduled Auction

                                                                                                    |
| -

                             | Regular trading

                                                                                                        |
# TRADE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                          | Standard CLOB trade

                                                                                                    |
| A

                             | Auction trade

                                                                                                          |
| b

                             | Apex Liquidity Provision order trade (buy side aggressor)

                                                              |
| B

                             | VBBO trade (buy side aggressor)

                                                                                        |
| C

                             | Closing cross trade

                                                                                                    |
| D

                             | Trade report subject to conditions other than market price

                                                             |
| L

                             | Late trade report

                                                                                                      |
| N

                             | Off-book, on-exchange trade

                                                                                            |
| O

                             | Opening cross trade

                                                                                                    |
| P

                             | Trade report from previous day

                                                                                         |
| s

                             | Apex Liquidity Provision order trade (sell side aggressor)

                                                             |
| S

                             | VBBO trade (sell side aggressor)

                                                                                       |
| U

                             | Uncrossing trade

                                                                                                       |
# UPDATE_TYPE - Enumeration

| Enumeration ID

                | Enumeration Description

                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
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

                             | Partial fill

